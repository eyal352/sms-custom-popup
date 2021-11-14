      function waitForElm(selector) {
          return new Promise(resolve => {
              if (document.querySelector(selector)) {
                  return resolve(document.querySelector(selector));
              }

              const observer = new MutationObserver(mutations => {
                  if (document.querySelector(selector)) {
                      resolve(document.querySelector(selector));
                      observer.disconnect();
                  }
              });

              observer.observe(document.body, {
                  childList: true,
                  subtree: true
              });
          });
      }
      //selector for input element
      waitForElm('input.needsclick.undefined.kl-private-reset-css-Xuajs1').then(elm => {
        //selector for submit button  
        let submitButton = document.querySelector(
          "button.needsclick.go596865934.kl-private-reset-css-Xuajs1");
          submitButton.onclick = function () {
              console.log("phone is " + elm.value);
              fetch('https://api.smsbump.com/v2/formsPublic/subscribe', {
                      method: 'POST',
                      body: JSON.stringify({
                          'form_id': #####,
                          'phone': elm.value,
                          'country': 'US',
                          'source': "popup"
                      }),
                      headers: {
                          'Content-Type': 'x-www-form-urlencoded',
                          'x-smsbump-platform': 'shopify',
                      }
                  })
                  .then(response => {
                      console.log(response);
                      response.json();
                  })
                  .then(data => {
                      console.log(data)
                  });

          }
      });
