# Fire Detection React Application
<p> 

## Steps
<br />
<b>Step 1.</b> Install App Depdendencies 
<pre>npm install</pre>
<br/><br/>
<b>Step 2.</b> Create a new free object storage repository on IBM Cloud <a href="https://cloud.ibm.com/objectstorage/create">Create Cloud Object Storage Bucket</a> 
<br/><br/>
<b>Step 3.</b> Create a new bucket and store model.json and .bin files into the bucket.</a> 
<img src="https://i.imgur.com/lN9lFLJ.png">
<br/><br/>
<b>Step 4.</b> Enable public access policy.</a> 
<img src="https://i.imgur.com/sstZfBG.png">
<br/><br/>
<b>Step 5.</b> Download and install the Cloud Object Store plugin.</a> 
<br/><br/>
<b>Step 6.</b> Login to the IBM Cloud CLI, target the right region and run the following command from inside of the TFODApp folder.</a> 
<pre>ibmcloud cos bucket-cors-put --bucket sayantfod --cors-configuration file://corsconfig.json</pre>
<br/><br/>
<b>Step 7.</b> Update the following line with the link to your model.json file inside of the cloud bucket.</a> 
<pre>
const net = await tf.loadGraphModel('YOUR MODEL.json file here')
// e.g. const net = await tf.loadGraphModel('https://sayantfod.s3.au-syd.cloud-object-storage.appdomain.cloud/model.json')
</pre>
This URI is available from your bucket. Select the model.json file then choose object details and the link will be made available. 
<img src="https://i.imgur.com/hdsg0fz.png">
<br/><br/>
<b>Step 10.</b> Update the labelmap inside of utilities.js with your labels.</a> 
<br/><br/>
<b>Step 11.</b> Start the app by running npm start.</a> 
<pre>npm start</pre>
<br/><br/>




