# rule-node-examples-ui-ngx

Configuration UI for IoToP Rule Nodes

## Build steps

1) Switch to iotop-rel-3.3 branch
    ```
    git checkout iotop-rel-3.3
    ```

2) Cleanup
    ```
    yarn run cleanup 
    ```
2) Get IoToP UI dependency
    ```
    yarn run getthingsboard 
    ```
3) Install dependencies
    ```
    yarn install 
    ```
4) Production build    
    ```
    yarn run build 
    ```
    Resulting JavaScript should be here:
    ```
    ./target/generated-resources/public/static/custom-nodes-config.js
    ```
5) Deploy Rule Nodes UI JavaScript code to iotop-rule-nodes

    Resulting **custom-nodes-config.js**
    should be copied to ```iotop-rule-nodes/src/main/resources/public/static/rulenode/```
    directory of iotop-rule-nodes repository.

6) Run Rule Nodes UI in hot redeploy mode

    ```
    yarn start
    ```
    
    By default, Rule Nodes UI will be available on port 5000 (http://localhost:5000)
