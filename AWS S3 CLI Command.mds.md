# AWS S3 CLI Commands

1. `aws s3 ls`
The output of this command lists all the existing buckets in the particular region.

2. `aws s3 ls s3://<bucket_name>`
The output of this command enlists all the objects in the specified s3 bucket.

3. `aws s3 ls s3://<bucket_name>/<folder_name>`
The output of this command enlists all the files in the specified folder of the corresponding bucket.

4. ` aws s3 mb s3://<bucket_name> `
aws s3 mb s3://<bucket_name> --region <region>
This command creates a new bucket of the specified name. If the region code is not included, then it takes into account the default region.

5. `aws s3 cp <local_filename> s3://<bucket_name>`
This command is used to upload the local file in the specified bucket. The file needs to be present in the current active directory in which the command is run. The storage class here is Standard.

6. `aws s3 cp <local_filename> s3://<bucket_name> --storage-class REDUCED_REDUNDANCY`
This command is used to upload the local file in the specified bucket in the specified storage class, REDUCED_REDUNDANCY. The file needs to be present in the current active directory in which the command is run. This is done when the file is less important and is not to be used frequently. 

7. `aws s3 sync . s3://<bucket_name>`
This command is used to sync the contents of the local folder with the specified bucket. The folder needs to be present in the current active directory in which the command is run. 

8. `aws s3 sync . s3://<bucket_name> --delete`
This command syncs the local folder with the S3 bucket with deletion. If any files are deleted from the local folder, the changes are reflected in the bucket as well after the execution of this command.

9. `aws s3 sync s3://<bucket_name> .`
This command is used to sync the specified S3 bucket with the local folder or the current local folder. If any files are updated to the S3 bucket from any other source, then they will be reflected to the local folder as well.

10. `aws s3 sync s3://<bucket_name> .  --delete`
This command syncs the S3 bucket to the local folder with deletion. If any files are deleted from the bucket, the changes are reflected in the current local folder  as well after the execution of this command.

11. `aws s3 sync . s3://<bucket_name> --exclude *.css`
This command syncs the local folder with the S3 bucket, however, it does not upload the files with .css extension. The specified extension files are excluded from the uploading process.

12. `aws s3 sync . s3://<bucket_name> --include *.css`
This command syncs the local folder with the S3 bucket including the files with the specified extension.

13. `aws s3 mv s3://<bucket_name> .  --recursive`
This command moves all the S3 bucket contents to the local active folder, thus making the bucket empty. The contents are moved and hence are deleted from the bucket. To ensure that the subdirectories are also moved, --recursive is also included in the command.

14. `aws s3 mv . s3://<bucket_name>  --recursive`
This command moves all the contents of the current local folder to the S3 bucket, thus making the local folder empty. The contents are moved and hence are deleted from the local folder. To ensure that the subdirectories are also moved, --recursive is also included in the command.

15. `aws s3 rb s3://<bucket_name>`
This command deletes the specified S3 bucket. However, this command works only when the bucket to be deleted is empty.

16. `aws s3 rb s3://<bucket_name> --force`
This command is executed when a S3 bucket has contents, i.e., files and folders and this bucket is required to be deleted. This command deletes the bucket along with contents inside it.  

