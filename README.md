# ckeditor-image-uploader-plugin
An open source plugin for CKEDITOR to upload images saved on your local machine.

# How to install?
- You can use this plugin with CKEDITOR. Configure it with an AJAX URL for uploading the images. You can add it in your config.js as follows:
`CKEDITOR.config.extraPlugins: 'simage'`  
`CKEDITOR.config.imageUploadURL: <INSERT URL>`

- You can listen to `imageUploading` event to do anything while the image is uploading. Similarly, there is an event `imageUploaded` to perform any action after image has successfully uploaded or the image upload failed.


