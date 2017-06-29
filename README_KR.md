# things-image-button

## 이는 이미지를 클릭하여 데이터를 호출하는 컴포넌트이다.

Example:

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

element의 종속성은 [Bower](http://bower.io/)를 통해 관리되며, 아래의 방법을 통해 설치할 수 있다.

    npm install -g bower

그리고, 아래의 방법을 통해 실행할 수 있다.

    bower install

## Playing With Your Element

element를 독립적으로 처리하려면 [Polyserve](https://github.com/PolymerLabs/polyserve)를 사용하여 element의 bower 의존성을 유지하도록 하며, 이는 아래의 방법을 통해 설치할 수 있다.

    npm install -g polymer-cli

그리고, 아래의 방법을 통해 실행할 수 있다.

    polymer serve

element를 실행한 경우, `things-image-button`이 디렉토리 이름으로 포함되어 있는 `http://localhost:8080/components/things-image-button/`을 통해 이를 미리 확인할 수 있다. 
