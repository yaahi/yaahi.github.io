+++
title = "Home"
+++

This is a simple javascript redirection library.

<div name="manualRedirectionDiv"/>

<script type="text/javascript">
{
    // https://github.com/sanskrit-lexicon/csl-ldev/blob/main/v02/mw/2.txt
    let mwSource = module_main.default.query.getParam("mw");
    if (mwSource) {
      module_main.default.redirectToPage(`https://github.com/sanskrit-lexicon/csl-ldev/blob/main/v02/mw/${mwSource}`);
    }

}

{
    let colognePage = module_main.default.query.getParam("cp");
    if (colognePage) {
      let dict = module_main.default.query.getParam("d");
      module_main.default.redirectToPage(`https://www.sanskrit-lexicon.uni-koeln.de/scans/csl-apidev/servepdf.php?dict=${dict}&page=${colognePage}`);
    }
}
</script>