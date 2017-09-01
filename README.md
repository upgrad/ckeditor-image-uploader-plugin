# ckeditor-image-uploader-plugin
An open source plugin for CKEDITOR to upload images saved on your local machine.

# How to install?
- You can use this plugin with CKEDITOR. Configure it with an AJAX URL for uploading the images. You can add it in your config.js as follows:

`CKEDITOR.config.extraPlugins: 'simage'`
`CKEDITOR.config.imageUploadURL: <INSERT URL>`

- You can listen to `preventFormSubmit` event to do anything while the image is uploading. One specific use case for this is to prevent form submit while the image is uploading. Similarly, there is a `enableFormSubmit` to perform any actions after image has successfully loaded or the image upload failed.


