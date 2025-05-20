# Background

Our online IDE stores versioned data in a database file system. Every change a student or teacher makes is stored as a separate version. Each version stores metadata for all the contained files and directories.

The metadata includes the following relevant data:

- `type`: The mime type of the file (`inode/directory` for directories).
- `name`: The name of the file or directory.
- `current`: is `true`, if this is the most current version of the file or directory.
- `key`: an ID for the file or directory. All versions of the same file have the same key.
- `permissions`: An object which stores the access rights ("read" for read access and "write" for write access).
- `children`: Only for directories: An array of keys from files or directories, which are currently children of this directory.

The root directory has the special name `"."`.

# Your task

Write your code in JavaScript or TypeScript, either for the browser or Node.js.

Provided an array of metadata objects as described above, your task is to display the project tree, as seen by a student at the current timepoint (`current === true`).

You are free to choose how you want to print the project tree (console is good enough for us).

If a student should not be able to read the file/directory, it should not show up in the project tree.

If a file/directory is readable but not writeable, append the name with " (r)".

# Provided files

You find an example dump from our database (data.json), and the expected outcome (expected_output.txt) in this repo.

# How to hand in

Send us your solution in a way you find the most suitable. 
