# azure-resume
My resume displayed via website using Azure resources. 

## First Steps - Frontend

- Frontend folder contains the original website template
- Added SSH keys to VSCode
- Added Resume details and adjusted links to personal sites
- main.js added for website visit counter
    ```js
    window.addEventListener('DOMContentLoaded', (event) =>{
    getVisitCount();
    })

    const functionApi = '';

    const getVisitCount = () => {
    let count = 30;
    fetch(functionApi).then(response => {
        return response.json()
    }).then(response => {
        console.log("Website called function API.");
        count = response.count;
        document.getElementById("counter").innerText = count;
    }).catch(function(error){
        console.log(error);
    });
    return count;
    }
    ```

## Next - Backend
