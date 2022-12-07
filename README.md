<h4>Creating a pipeline from scratch using Jenkins and GitLab</h4>

Go to Dashboard and click the ```+ New Item``` selection

![alt text](./images/1.png)

Enter a name for your pipeline, and select ```Pipeline``

![alt text](./images/2.png)

Scroll down to build triggers and click ```Build when a change is pushed to GitLab```

![alt text](./images/3.png)

Now head to your GitLab repository and click ```Settings > Webhooks```

![alt text](./images/4.png)

Head back to Jenkins, and copy the GitLab webhook URL

![alt text](./images/5.png)

Head back to your GitLab Webhooks, and paste the URL into the bar

Make sure to change ```http://``` into ```https://```

![alt text](./images/6.png)

Scroll down and click ```Advanced```

![alt text](./images/7.png)

Continue scrolling down until you see ```Secret Token``` then click ```Generate```

Copy the token to your clipboard

![alt text](./images/8.png)

Head back to GitLab Webhooks and paste the secret token in

![alt text](./images/9.png)

Scroll down and click ```Add Webhook```

![alt text](./images/10.png)

Go back to Jenkins, scroll down to the Pipeline section

Select ```Pipeline script from SCM```

![alt text](./images/11.png)

Select ```Git```

![alt text](./images/12.png)

Select your credentials

![alt text](./images/13.png)

Go back to GitLab Repository, go to ```Clone``` and copy ```Clone with HTTPS```

![alt text](./images/14.png)

Paste it into Repository URL

![alt text](./images/15.png)

Scroll down to ```Branches to build``` and change the default ```*/master``` into ```*/main```

![alt text](./images/16.png)

Scroll down to script path and change the default ```Jenkinsfile``` to ```ci/Jenkinsfile```

![alt text](./images/17.png)

Now as long as you have a Jenkinsfile at ```ci/Jenkinsfile``` in your GitLab repisitory, the pipeline should run on any git commit

![alt text](./images/18.png)