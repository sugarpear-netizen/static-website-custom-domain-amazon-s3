**Configure a Static Website with Amazon S3**

Below is documentation of stated project as part of attempt to build beginner friendly project with AWS.
The exact documentation can be found here: https://go.aws/3adlSpe  

---

**Step 1: Create two buckets**
1. Sign in to the AWS Management Console and open S3 console at https://console.aws.amazon.com/s3/
2. Create your root domain bucket: Select bucket name, choose region geographically close to minimize latency, accept default settings and create.  <details><summary>Display</summary> <img src="https://user-images.githubusercontent.com/77137903/171223285-f5118759-fcdf-4b2a-93b6-1c4592b5e246.png" /> </details>  
3. Repeat 2 for subdomain bucket:  <details><summary>Display</summary><img src="https://user-images.githubusercontent.com/77137903/171224472-dde93f63-5dfe-4fa1-972a-7cadd75c72b4.png" /></details>

**Step 2: Configure your root domain bucket for website hosting**
1. Choose name of bucket you want to enable static website hosting for in S3 console.  <details><summary>Display</summary><img src="https://user-images.githubusercontent.com/77137903/171225510-7928f48f-1143-4d4e-a89f-452cce85eba8.png" /></details>
2. Choose properties, edit static website hosting and select "Host a static website".  <details><summary>Display</summary><img src="![image](https://user-images.githubusercontent.com/77137903/171226206-19a470bb-befc-4928-ab03-d7dcc6a5cb59.png" /></details>
3. Enter file name for index and error document and finally save changes.  <details><summary>Display</summary><img src="https://user-images.githubusercontent.com/77137903/171226566-487bfcf3-17f3-4f9e-986b-434e0e529787.png" /></details>


**Step 3: Configure your subdomain bucket for website redirect**
1. Choose your subdomain bucket name.  <details><summary>Display</summary><img src="https://user-images.githubusercontent.com/77137903/171228883-936e4da2-fac3-4679-8e24-6038c33ef87d.png" /></details>
2. Choose properties, edit static website hosting and select "Redirect requests for an object".  <details><summary>Display</summary><img src="https://user-images.githubusercontent.com/77137903/171229191-12465d32-a7d6-462a-bd41-06128404fe5e.png" /></details>
3. In Host name, enter your root domain. Then, select "http" for Protocol. Finally, save changes.  <details><summary>Display</summary><img src="https://user-images.githubusercontent.com/77137903/171229566-8a1046a9-c13d-40a9-89e0-f50db266c777.png" /></details>

