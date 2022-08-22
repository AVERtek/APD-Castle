# "REWRITE YOUR OWN FAIRYTALE" <!-- Loads <model-viewer> for old browsers like IE11: -->
  <h1 style="text-align: center;" markdown="1"> It's Time to Modernize Your Castle with Resort Style Living!</h1>
  <script nomodule="" src="https://unpkg.com/@google/model-viewer/dist/model-viewer-legacy.js">
  </script>
  
  <!-- The following libraries and polyfills are recommended to maximize browser support -->  
  <!-- REQUIRED: Web Components polyfill to support Edge and Firefox < 63 -->
  <script src="https://unpkg.com/@webcomponents/webcomponentsjs/webcomponents-loader.js"></script>

  <!-- OPTIONAL: Intersection Observer polyfill for better performance in Safari and IE11 -->
  <script src="https://unpkg.com/intersection-observer/intersection-observer.js"></script>

  <!-- OPTIONAL: Resize Observer polyfill improves resize behavior in non-Chrome browsers -->
  <script src="https://unpkg.com/resize-observer-polyfill/dist/ResizeObserver.js"></script>

  <!-- OPTIONAL: Fullscreen polyfill is required for experimental AR features in Canary -->
  <!--<script src="https://unpkg.com/fullscreen-polyfill/dist/fullscreen.polyfill.js"></script>-->

  <!-- OPTIONAL: Include prismatic.js for Magic Leap support -->
  <!--<script src="https://unpkg.com/@magicleap/prismatic/prismatic.min.js"></script>-->

  
  <script>
      function Sync(selector, audioSelector) {
        var modelViewer = document.querySelector(selector);
        var sound = document.querySelector(audioSelector);
        var playRequest = document.querySelector("#overlay");

   sound.addEventListener("timeupdate", () => {
          modelViewer.currentTime = sound.currentTime;
          console.log("modelViewer time: " + modelViewer.currentTime);
        });

   sound.addEventListener("pause", () => {
          modelViewer.pause();
        });

   sound.addEventListener("play", () => {
          modelViewer.play();

   playRequest.classList.add("hide");
        });

   document.addEventListener("visibilitychange", () => {
          if (document.visibilityState !== "visible") {
            sound.pause();
          }
        });

   var promise = sound.play();
        if (promise !== undefined) {
          promise
            .then(_ => {
              console.log("Autoplay has worked");
              playRequest.classList.add("hide");
            })
            .catch(error => {
              // Show a "Play" button so that user can start playback.
              console.log("Autoplay has not worked");

   // show the modal dialogue to play this
   playRequest.classList.remove("hide");
            });
        }

   }

   function playNow() {
        var playRequest = document.querySelector("#overlay");
        playRequest.classList.add("hide");

   var sound = document.querySelector("#sound");
        sound.play();
      }

   function jumpTo(time) {
        var sound = document.querySelector("#sound");
        sound.currentTime = time;
      }
   </script>

<model-viewer id="reveal" loading="eager" id="paused-change-demo" camera-controls camera-orbit="0deg 45deg 120m" autoplay animation-name="TheLife" ar shadow-intensity="1" src="ModelsCastle/scene.gltf" ar="" ar-modes="scene-viewer webxr quick-look" ios-src="Medieval_Fantasy_Book.usdz" alt="We Wrote the Book on Home & Auto Protection" ar-scale="auto" camera-controls="" style="width: 100%; height: 500px" exposure="0.5"> <button slot="ar-button" style="background-color: white; border-radius: 8px; border: 1 px solid black; position: absolute; top: 20px; right: 20px; ">
      👋 AR Click Here
  </button>
</model-viewer>

<section class="attribution">
        <div>
          <span>
            <h1 style="text-align: center;" markdown="1">Play Music</h1>
              <p align="center">
              <span>
              <audio controls autoplay loop id="sound">
                <source src="Sound/Chasing the Sunshine - 30.mp3"/>
              </audio
            ></span> 
             </p>
            </span>
         </div>
   </section>
   <script>
        window.addEventListener("load", () => {
          Sync("#model-viewer", "#sound");
        });
      </script>
   

<script>
/**
* Function that registers a click on an outbound link in Analytics.
* This function takes a valid URL string as an argument, and uses that URL string
* as the event label. Setting the transport method to 'beacon' lets the hit be sent
* using 'navigator.sendBeacon' in browser that support it.
*/
var getOutboundLink = function(url) {
  gtag('event', 'click', {
    'event_category': 'outbound',
    'event_label': url,
    'transport_type': 'beacon',
    'event_callback': function(){document.location = url;}
  });
}
</script>

<!-- Loads <model-viewer> for modern browsers: -->
 <script type="module" src="https://unpkg.com/@google/model-viewer/dist/model-viewer.js">
  </script>
<script nomodule="" src="https://unpkg.com/@google/model-viewer/dist/model-viewer-legacy.js"></script>
<script src="{{ "/assets/js/scale.fix.js" | relative_url }}"></script>

<!-- Loads <model-viewer> for modern browsers: -->
 <script type="module" src="https://unpkg.com/@google/model-viewer/dist/model-viewer.js">
  </script>
<script nomodule="" src="https://unpkg.com/@google/model-viewer/dist/model-viewer-legacy.js"></script>

---

<h3 style="text-align: center;" markdown="1"><a href="https://avertek.net/" onclick="getOutboundLink('https://avertek.net/'); return false;">Learn More About AVERtek's XR-NOW</a></h3> 
  <br><br>
