# My ReadMe file to define important steps (MAC)

- Install K6
    -- brew install k6
- Run k6
    -- k6 run `name_of_file`
- To ramp the number of VUs up and down during the test, use the options.stages property. As below
    ```
    export const options = {
        stages: [
            { duration: '30s', target: 20 },
            { duration: '1m30s', target: 10 },
            { duration: '20s', target: 0 },
        ],
    };
    ```