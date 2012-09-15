# friend-oauth2-examples

Includes Facebook and App.net examples using [Friend-OAuth2](https://github.com/ddellacosta/friend-oauth2), an OAuth2 workflow for [Friend](https://github.com/cemerick/friend).

## Running

Tweak the project.clj file if the handler you want to try is commented out.

```clojure
  :ring {:handler friend-oauth2-examples.facebook-handler/app}
;;  :ring {:handler friend-oauth2-examples.appdotnet-handler/app}
```

Configure your client id/secret and callback url in the handler code.

```clojure
(def client-config
  {:client-id "<HERE>"
   :client-secret "<HERE>"
   :callback {:domain "http://<HERE>" :path "/<AND HERE>"}})
```

At that point, you should be able to start it up using lein:

    lein ring server(-headless)

## License

Distributed under the MIT License (http://dd.mit-license.org/)