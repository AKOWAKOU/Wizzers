### Setup Projetc
        git clone git@github.com:AKOWAKOU/wittzers.git

        cd backend

### Install Requirements

    ""bash""

    python -m venv env

    source env/bin/active

    ""Windows""

    python -m venv myenv   
    virtualenv myenv      (encas de virtualenv installer sur la machine)

    .\myenv\Scripts\activate


    pip install -r requirements.txt

    flask run 

    tester L'api sur http://localhost:5000


### Test Postman

    1. Endpoint : /predict
    Méthode : POST
    URL : http://localhost:5000/predict
    Headers :
            {
                "Content-Type": "application/json"
            }

    Body (JSON) :
            {
                "text": "Test input"
            }

    Attendue:
            {
                "result": "Result: Test input"
            }
        

    2. Endpoint : /uploadocassion

    Méthode:POST
    URL:http://localhost:5000/uploadocassion
    Headers:
            {
                "Content-Type": "multipart/form-data"
            }
    
    Body (form-data) :
            uploadedFile : (Fichier image)
            url : https://example.com/image.png

    Attendue:
            {
                "message": "Result image copied successfully."
            }



    3. Endpoint : /uploado

    Méthode:POST
    URL:http://localhost:5000/upload
    Headers:
            {
                "Content-Type": "multipart/form-data"
            }
    
    Body (form-data) :
            uploadedFile : (Fichier image)

    Attendue:
            {
                "message": "Result image copied successfully."
            }



    4. Endpoint : /handleprompt
    Méthode : POST
    URL : http://localhost:5000/handleprompt
    Headers :
            {
                "Content-Type": "application/json"
            }


    Body (JSON) :
                {
                    "prompt": "Generate a stylish outfit"
                }

    Attendue:
            {
                "message": "Success"
            }
            
        
    5. Endpoint : /handleocassion
    Méthode : POST
    URL : http://localhost:5000/handleocassion
    Headers :
        {
                "Content-Type": "application/json"
        }

    Body (JSON) :
            {
                "color": "blue",
                "selectedOccasion": "wedding"
            }

    Attendue:
        {
            "newItems": ["item1", "item2"],
            "showRecommendations": true
        }        