# concession-kiosk-backend

This is the backend component for the concession kiosk application. The backend is written using Node.js and Express and will serve as the intermediary between the frontend and the database.

# How to Deploy on OpenShift

- oc new-project concession-kiosk

- oc new-app https://github.com/IndraniDey1/concession-kiosk-backend --name backend

- oc get svc backend

- oc new-app --template=mongodb-ephemeral

- oc set env dc/backend MONGODB_URL=mongodb://someuser:some-password@mongodb/sampledb

- oc create -f apply config-example.json.   ( see this file in 'example' folder. This is to create configmap)

-oc set env dc/backend --from configmap/config






