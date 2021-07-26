# image-lambda

## Description of how to use Lambda

  When an image is uploaded to your S3 bucket, it should trigger a Lambda function which must:

- Download a file called “images.json” from the S3 Bucket if it exists

- The images.json should be an array of objects, each representing an image. 
- Create an empty array if this file is not present
- Create a metadata object describing the image's Name, Size, Type, etc.
- Append the data for this image to the array

  ***Note***: If the image is a duplicate name, update the object in the array, don’t just add it
  Upload the images.json file back to the S3 bucket

## Issues

  Don't know how to use aws-sdk.
