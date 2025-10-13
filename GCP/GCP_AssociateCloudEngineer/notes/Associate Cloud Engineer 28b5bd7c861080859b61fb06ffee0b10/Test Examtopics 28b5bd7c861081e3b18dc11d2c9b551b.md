# Test Examtopics

You need to set up permissions for a set of Compute Engine instances to enable them to write data into a particular Cloud Storage bucket. You want to follow

Google-recommended practices. What should you do?

- A. Create a service account with an access scope. Use the access scope 'https://www.googleapis.com/auth/devstorage.write_only'.
- B. Create a service account with an access scope. Use the access scope 'https://www.googleapis.com/auth/cloud-platform'.
- C. Create a service account and add it to the IAM role 'storage.objectCreator' for that bucket.
- D. Create a service account and add it to the IAM role 'storage.objectAdmin' for that bucket.

---

You need to run an important query in BigQuery but expect it to return a lot of records. You want to find out how much it will cost to run the query. You are using on-demand pricing. What should you do?

- A. Arrange to switch to Flat-Rate pricing for this query, then move back to on-demand.
- B. Use the command line to run a dry run query to estimate the number of bytes read. Then convert that bytes estimate to dollars using the Pricing Calculator.
- C. Use the command line to run a dry run query to estimate the number of bytes returned. Then convert that bytes estimate to dollars using the Pricing Calculator.
- D. Run a select count (*) to get an idea of how many records your query will look through. Then convert that number of rows to dollars using the Pricing Calculator.

### 🔍 ¿Qué es un *dry run*?

Un ***dry run*** es una validación de consulta en la que BigQuery **analiza la consulta** y **calcula cuántos bytes tendría que leer**, **pero no ejecuta la consulta ni accede a los datos reales**.

---

You need to set up a policy so that videos stored in a specific Cloud Storage Regional bucket are moved to Coldline after 90 days, and then deleted after one year from their creation. How should you set up the policy?

- A. Use Cloud Storage Object Lifecycle Management using Age conditions with SetStorageClass and Delete actions. Set the SetStorageClass action to 90 days and the Delete action to 275 days (365 ג€" 90)
- B. Use Cloud Storage Object Lifecycle Management using Age conditions with SetStorageClass and Delete actions. Set the SetStorageClass action to 90 days and the Delete action to 365 days.
- C. Use gsutil rewrite and set the Delete action to 275 days (365-90).
- D. Use gsutil rewrite and set the Delete action to 365 days.

You can change the storage class of an existing object either by rewriting the object or by using Object Lifecycle Management...Since Object Life cycle management was used there was no need to recalculate the expiration date and delete action still remains 365 days.

---