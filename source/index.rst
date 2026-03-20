.. ReadTheDocs_Test documentation master file, created by
   sphinx-quickstart on Thu Mar 19 15:21:08 2026.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

ReadTheDocs_Test documentation
==============================

Add your content using ``reStructuredText`` syntax. See the
`reStructuredText <https://www.sphinx-doc.org/en/master/usage/restructuredtext/index.html>`_
documentation for details.


.. toctree::
   :maxdepth: 2
   :caption: Contents:


.. raw:: html

    <div id="giscus_container" style="margin-top: 50px;"></div>

    <script src="https://giscus.app/client.js"
        data-repo="Mingliang-Liu/readthedoctest"
        data-repo-id="R_kgDORrEgmQ"
        data-category="Announcements"
        data-category-id="DIC_kwDORrEgmc4C4wu9"
        data-mapping="title"
        data-strict="0"
        data-reactions-enabled="0"
        data-emit-metadata="0"
        data-input-position="up"
        data-theme="light"
        data-lang="zh-CN"
        crossorigin="anonymous"
        async>
    </script>

    <script>
      function updateGiscusTheme() {
         const theme = document.documentElement.getAttribute("data-color-mode");
         const giscusFrame = document.querySelector("iframe.giscus-frame");

         if (!giscusFrame) return;

         giscusFrame.contentWindow.postMessage({
                  giscus: {
                     setConfig: {
                           theme: theme === "dark" ? "dark" : "light"
                     }
                  }
               },
               "https://giscus.app"
         );
      }

      // 初始执行
      window.addEventListener("load", updateGiscusTheme);

      // 监听主题切换（关键）
      const observer = new MutationObserver(updateGiscusTheme);
      observer.observe(document.documentElement, {
         attributes: true,
         attributeFilter: ["data-color-mode"]
      });
    </script>