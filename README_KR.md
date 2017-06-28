## things-image-button
이미지 클릭하여 data 호출하는 컴퍼넌트.

### Example:

```html
		<things-image-button item="[[item]]" title="[[title]]" image-src="[[imagepath]]">
		</things-image-button>
```
### Detail:
```html
			   <sample-image-button></sample-image-button>
			   <dom-module id="sample-image-button">
			   <template>
  		   <things-image-button  id="imagebutton" item ="[[item]]" title ="[[title]]" image-src ="[[imagepath]]">
	       </things-image-button>
			         Data: [[imagedata]]
			       </template>
			       <script>
			        Polymer({
			          is: 'sample-image-button',
			          ready:function(){
			               this.imagepath="./image1.png",
			               this.title="Pokemon",
			               this.item={
			                   name:"Bee",
			                   color:"yellow"
			               }
			             },
			             listeners: {
			               'imagebutton.things-image-button-tap': "imageTap",
			             },
			             imageTap:function(event){
			               console.log(event);
			               this.imagedata= JSON.stringify(event.detail);
			             }
			          });
			     </script>
			     </dom-module>
```


## Dependencies

Element dependencies are managed via [Bower](http://bower.io/). You can
install that via:

    npm install -g bower

Then, go ahead and download the element's dependencies:

    bower install

## Playing With Your Element

If you wish to work on your element in isolation, we recommend that you use
[Polyserve](https://github.com/PolymerLabs/polyserve) to keep your element's
bower dependencies in line. You can install it via:

    npm install -g polymer-cli

And you can run it via:

    polymer serve

Once running, you can preview your element at
`http://localhost:8080/components/things-alarm/`, where `things-alarm` is the name of the directory containing it.
