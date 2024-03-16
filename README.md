# scala-code-for-extracting-zip-in-adb

This document outlines the steps to handle a ZIP file within Databricks using Scala.

1. Check for the existence of a ZIP file named "sample_archive.zip" in the DBFS location "/mnt/flights/".
2. If the file exists, the script prints a confirmation message including the path of the ZIP file in DBFS.
3. A temporary directory is created in the local filesystem of the Databricks cluster to temporarily store the ZIP file.
4. The ZIP file is then copied from DBFS to the newly created temporary directory.
5. The script checks if the ZIP file has been successfully copied to the temporary directory.
6. If the copy is successful, the ZIP file is unzipped using a shell command within the temporary directory.
7. The output of the unzip command is printed, showing the result of the extraction process.
8. Optionally, the files present in the temporary directory after extraction are listed and their names are printed.
9. The script then filters out any .zip and .crc files from the extracted contents.
10. The remaining files (after filtering out .zip and .crc files) are copied back to a specified directory in DBFS.
11. For each file copied back to DBFS, a confirmation message is printed showing the source and destination paths.
12. Finally, the temporary directory in the local filesystem is cleaned up, removing all its contents.

This process ensures that the ZIP file is handled securely and efficiently within the Databricks environment, from checking its existence to extracting its contents and managing the temporary storage used during the process.
