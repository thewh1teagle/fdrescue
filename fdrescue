#!/usr/bin/python3

import os
import subprocess
import sys


def usage(argv):
    if len(sys.argv) < 3:
        sys.exit("Usage: ./{} infolder outfolder".format(sys.argv[0]))
    else:
        print("Welcome to fdrescue!")

def rescue(infolder, outfolder):
    for root, _dirs, files in os.walk(infolder):
        if not files:
            continue
        root = os.path.relpath(root, infolder)
        outpath = os.path.join(outfolder, root)
        if not os.path.exists(outpath):
            os.makedirs(outpath)
        for file in files:
            subprocess.call(['ddrescue'] + sys.argv[1:-2] +
                    [os.path.join(infolder, root, file), os.path.join(outpath,
                        file)])


if __name__ == "__main__":
    usage(sys.argv)
    infolder = sys.argv[-2]
    outfolder = sys.argv[-1]
    rescue(infolder, outfolder)
