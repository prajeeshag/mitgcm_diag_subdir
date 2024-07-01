To address the issue of MITgcm runs hanging when running in Shaheen III due to the large number of files it creates, one solution is to output files into subdirectories.

The source code in the repository is to output diagnostic files into subdirectories corresponding to their file prefixes. For example, `diagA.0000000100.data[.meta]` will be written to a directory named `diagA/`.

The same approach is applied to time-averaged variables `[ETAtave, Ttave, Stave, uVeltave, vVeltave, wVeltave]` in `timeave_statv_write.F`. All other time-averaged fields are commented out.






