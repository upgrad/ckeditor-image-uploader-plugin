# ckeditor-image-uploader-plugin
An open source plugin for CKEDITOR to upload images saved on your local machine.

# How to install?
- You can use this plugin with CKEDITOR. Configure it with an AJAX URL for uploading the images. You can add it in your config.js as follows:
`CKEDITOR.config.extraPlugins: 'simage'`  
`CKEDITOR.config.imageUploadURL: <INSERT URL>`
`CKEDITOR.config.dataParser: func(data)`

- The response returned by your `imageUploadURL` should be of the type `Object` with the keys ordered in the increasing order of image resolution and the last key should be the original `src`. An example of `data` object is as below:
`{
	1x: {url:'someurl', ...},
	2x: {url:'someurl', ...},
	3x: {url:'someurl', ...},
	4x: {url:'someurl', ...},
	original: {url:'someurl', ...}
}`

- You can also use `srcset` attribute to display the image based on  resolution of the display. This is `optional`, in case you don't specify `srcset` attribute it will pick up the image from `src`. Set the `srcSet` attribute in config and assign it to a function which accepts `data` which is returned by your AJAX url and return the `string` for `srcset` attribute. Add the following statement in config.js to enable `srcset`:
`config.srcSet: func(data)`
The above function should return a `string` of the following form:
`"image-1x.png 1x, image-2x.png 2x, image-3x.png 3x, image-4x.png 4x"`
	
- You can listen to `preventFormSubmit` event to do anything while the image is uploading. One specific use case for this is to prevent form submit while the image is uploading. Similarly, there is an event `enableFormSubmit` to perform any action after image has successfully uploaded or the image upload failed.


