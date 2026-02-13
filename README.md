**zoomcamp-module-four-homework**

This repo consist of the dbt project used during the module and UPLOAD_TO_GCP folder which contains dockerized pipeline to download and upload files to google cloud

****Homework answers:****



**Question 1.**

	int_trips_unioned only as there are no + signs next to the model name
	
	Answer: int_trips_unioned only

	
**Question 2.**

	The test will return non zero code as the new value isnt present in the test case
	
	Answer: dbt will fail the test, returning a non-zero exit code

**Question 3.**

<img width="745" height="765" alt="image" src="https://github.com/user-attachments/assets/97ffbee4-8dfd-4d40-bad9-1c29a3c034cc" />
	
	Answer: 12,184

**Question 4.**

<img width="873" height="803" alt="image" src="https://github.com/user-attachments/assets/3411a408-7b3e-4af0-a56b-17d9f87523de" />

	Answer: East Harlem North

**Question 4.**

<img width="979" height="761" alt="image" src="https://github.com/user-attachments/assets/18bf7ca3-3da7-446d-b2cb-4c7cd0f75504" />

	Answer: 384,624

**Question 5.**
	
<img width="716" height="441" alt="image" src="https://github.com/user-attachments/assets/66242530-bcae-452f-b617-0536251c2754" />

<img width="578" height="750" alt="image" src="https://github.com/user-attachments/assets/8971090c-c280-4fab-8bb1-d304c1236cf3" />

	Answer: 43,244,693




How to run:

    Install gcp cli:
        curl -sSL https://sdk.cloud.google.com | bash

    Login to GCP:
        gcloud auth login
        gcloud auth login --impersonate-service-account=SERVICE_ACCOUNT_EMAIL

    Build docker image:
        docker build -t upload_to_gcp .

    Run docker:
        docker run --rm \
        -v $HOME/.config/gcloud:/root/.config/gcloud \
        upload_to_gcp ##upload_to_gcs.py 
                      ##upload_fnv_to_gcs.py -choose one depening on which file is to be uploaded
