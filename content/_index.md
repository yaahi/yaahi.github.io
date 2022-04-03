+++
title = "Home"
+++

This is a simple javascript redirection library.

<div name="manualRedirectionDiv"/>

<script type="text/javascript">
{
  // - https://yaahi.github.io/?d=mw&e=2 redirects to https://github.com/sanskrit-lexicon/csl-ldev/blob/main/v02/mw/2.txt
  let editPage = module_uiLib.default.query.getParam("e");
  if (editPage) {
    let dict = module_uiLib.default.query.getParam("d");
    module_uiLib.default.navigation.redirectToPage(`https://github.com/sanskrit-lexicon/csl-ldev/blob/main/v02/${dict}/${editPage}.txt`);
  }

}

{
  // https://yaahi.github.io/?cp=0001-a&d=MW72 redirects to https://www.sanskrit-lexicon.uni-koeln.de/scans/csl-apidev/servepdf.php?dict=MW72&page=0001-a?debugInfo=
  let colognePage = module_uiLib.default.query.getParam("cp");
  if (colognePage) {
    let dict = module_uiLib.default.query.getParam("d");
    module_uiLib.default.navigation.redirectToPage(`https://www.sanskrit-lexicon.uni-koeln.de/scans/csl-apidev/servepdf.php?dict=${dict}&page=${colognePage}`);
  }
}
</script>