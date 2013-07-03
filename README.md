## Quickstart to run GlassFish 4 on OpenShift##

GlassFish 4 is reference implementation of Java EE 7. Below are the steps required to run GlassFish4 on OpenShift. The sample running GlassFish 4 on OpenShift is available at http://glassfish4-t20.rhcloud.com/ and http://glassfish4-t20.rhcloud.com/hello

1. First create OpenShift diy application with name glassfish4
```
rhc app create glassfish4 diy
```

2. Add git remote to GlassFish4 OpenShift quickstart and pull code from it.
```
cd glassfish4
git remote add upstream https://github.com/shekhargulati/glassfish4-openshift-quickstart.git
git pull -s recursive -X theirs upstream master
```

3. Push the code to OpenShift. It will take atleast couple of minutes to start GlassFish 4. So be patient.
```
git push
```

4. Check the GlassFish 4 is up and running by going to http://glassfish-{domain}.rhcloud.com. Replace domain with your own domain name.

5. The sample app is also deployed. You can view the sample app under http://glassfish-{domain}.rhcloud.com/hello

## Limitations

1. Currently admin console does not work

2. This is not designed for scaling. OpenShift DIY applications does not scale.


