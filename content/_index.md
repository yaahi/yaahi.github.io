+++
title = "Home"
+++

<div name="manualRedirectionDiv"/>

<script>
    function redirectToPage(url, manualRedirectionDiv, dryRun, debugInfo="") {
        if (manualRedirectionDiv) {
            // TODO: The below has no visible effect.
            manualRedirectionDiv.innerHTML = `Redirecting <a href='${url}'>here</a>`;
        }
        if (url && !dryRun) {
            window.location.replace(url + `?debugInfo=${debugInfo}`);
        }
    }

    let mwSource = module_main.default.query.getParam("mw");
    if (mwSource) {
      redirectToPage(`https://github.com/sanskrit-lexicon/csl-ldev/blob/main/v02/mw/${mwSource}`);
    }

    let colognePage = module_main.default.query.getParam("cp");
    if (colognePage) {
      let dict = module_main.default.query.getParam("d");
      redirectToPage(`https://www.sanskrit-lexicon.uni-koeln.de/scans/csl-apidev/servepdf.php?dict=${dict}&page=${colognePage}`);
    }

</script>