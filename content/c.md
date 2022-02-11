+++
title = "Cologne redirection"
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

    let url = new URL(document.location.href);
    url.
    redirectToPage(window.location.href.replace("yaahi.github.io", "github.com/sanskrit-lexicon/csl-ldev/blob/main/v02"), document.getElementsByName("manualRedirectionDiv"), false);
</script>