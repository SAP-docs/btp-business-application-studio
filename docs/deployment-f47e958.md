<!-- loiof47e9586bcd64a10a0b44a3e6f7c41e5 -->

# Deployment

Steps you can take if you have trouble deploying an application.



<a name="loiof47e9586bcd64a10a0b44a3e6f7c41e5__section_hhz_txt_2dc"/>

## MTAR Deployment Fails

**Reason**

The MTAR deployment may fail because of a conflict in the `package-lock.json` file or because there is a need to deploy the MTAR without `node_modules`.

**Solution**

Disable the SAP Business Application Studio npm cache by setting the `.npmrc` file on the project level and setting the npm public registry in this file.

