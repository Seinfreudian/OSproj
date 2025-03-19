# OSproj
Self-restoring file systems that combat anti-forensic files infected by ransomware
In this file we modify mkfs to include a journaling mechanism to track changes(unauthorised or authorised) made to a file(journaling) and deleted files are replaced with random data. fsck then detects and reconstructs deleted files and tampered forensic evidence. This is a part of user end manipulation.
On the part of randomware, we develop a mutating virus (worm) that mutates at every execution. fsck detects these mutations of files and removes them, reverting the changes made. It does so by analyzing logs.
mkfs creates fake files and directories to detect malware activity, it monitors access, modifications and deletion of decoy files.
