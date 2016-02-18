<!DOCTYPE html>
<!--

    CollabNet TeamForge(r)
    Copyright 2007-2014 CollabNet, Inc. All rights reserved.
    http://www.collab.net

-->
<html data-ng-app="ctf" xmlns="http://www.w3.org/1999/xhtml" lang="en">
  <head>
    <meta charset="utf-8">
    <title data-ng-bind="$root.page_title">TeamForge</title>
    <base href="/ctf/" target="_blank"><!--[if lt IE 10]></base><![endif]-->
    <link rel="shortcut icon" href="images/icons/favicon.ico" />
    <link rel="stylesheet" href="/css/header_footer_common.css" type="text/css" />
    <link href="/css/font-awesome.min.css" type="text/css" rel="stylesheet">
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />

    <!--[if lt IE 10]>
    <script type="text/javascript">
      (function() {
        var baseTag = document.getElementsByTagName('base')[0];
        baseTag.href = baseTag.href;
      })();
    </script>
    <![endif]-->
    <!--[if lt IE 9]>
    <script src="js/polyfill/ie8.js"></script>
    <script src="js/polyfill/dropfile.js"></script>
    <![endif]-->
    <!--[if lte IE 9]>
    <script>
      var key = window.location.search.substring(1).split('=')[0],
      master = window.location.search.substring(1).split('=')[1];
      // Set only if invoked by xdomain from thirdparty[top_include.jsp] pages
      if (master && key === 'xdMaster') {
      	var xdomainElem = document.createElement('script'),
      	      attr = document.createAttribute("master");
      	xdomainElem.src = '/ctf/js/thirdparty/domain/xdomain.js';
        attr.value = master;
        xdomainElem.setAttributeNode(attr);
        document.getElementsByTagName('base')[0].parentNode.insertBefore(xdomainElem, document.getElementsByTagName('base')[0].nextSibling);
      }
    </script>
    <![endif]-->
    <link rel="stylesheet" href="js/polyfill/ie_styles.css" type="text/css" />
    <link rel="stylesheet" href="css/all-thirdparty.css" type="text/css" />
    <link rel="stylesheet" href="css/all-common.css" type="text/css" />
    <link rel="stylesheet" href="css/all-ctf.css" type="text/css" />
    <link rel="stylesheet" href="/ctf/api/main/css-customization" type="text/css" />
    <script src="js/all-in-one.js" type="text/javascript"></script>
    <script src="js/all-in-one-saturn.js" type="text/javascript"></script>
    <!-- reports module dependencies -->
    <script src="js/thirdparty/highcharts/js/adapters/standalone-framework.js" type="text/javascript"></script>
    <script src="js/thirdparty/highcharts/js/highcharts.js" type="text/javascript"></script>
    <script src="js/thirdparty/highcharts/js/highcharts-more.js" type="text/javascript"></script>
    <script src="js/thirdparty/highcharts/modules/exporting.js" type="text/javascript"></script>
    <script src="js/thirdparty/highcharts/modules/drilldown.js" type="text/javascript"></script>
    <script src="js/thirdparty/angular-file-upload/ng-file-upload.min.js" type="text/javascript"></script>
    <!--[if lte IE 9]><script src="js/thirdparty/angular-file-upload/ng-file-upload-shim.min.js" type="text/javascript"></script><![endif]-->
    <script src="js/thirdparty/ng-tags-input/ng-tags-input.min.js" type="text/javascript"></script>
    <script src="/ctf/api/main/js-customization" type="text/javascript"></script>
  </head>
  <body class="ctf_7_x_styles" >
  <div data-ctf></div>
  </body>
</html>
