# angular-editor

<strong>演示地址：</strong><a href="http://gongshunkai.github.io/demo/angular-editor/test-angular.html">http://gongshunkai.github.io/demo/angular-editor/test-angular.html</a>

<h4>使用方法：</h4>


&lt;link rel="stylesheet" type="text/css" href="bootstrap/css/bootstrap.min.css"&gt;
&lt;link rel="stylesheet" href="bootstrap/css/font-awesome.min.css"&gt;
&lt;link rel="stylesheet" type="text/css" href="editor.css"&gt;

&lt;script src="editor.js"&gt;&lt;/script&gt;
&lt;script src="libs/angular.js"&gt;&lt;/script&gt;
&lt;script src="libs/angular-editor.js"&gt;&lt;/script&gt;
		

		
&lt;div ng-app="webapp" ng-controller="TestCtrl"&gt;
	&lt;ng-editor content="test"&gt;&lt;/ng-editor&gt;
&lt;/div>
		


		


	angular.module('webapp', [
		'ngEditor'
	])
	.config(['editorConfig',function(editorConfig) {
		editorConfig.height = 200;
		editorConfig.toolbarButtons = ['bold','italic','fontFamily','fontSize','formatBlock','color','|','align','|','createLink','insertImage','|','fullScreen','codeView'];
	}])
	.controller('TestCtrl', ['$scope', function($scope){
		$scope.test = '&lt;p&gt;test content&lt;/p&gt;';
	}]);


	