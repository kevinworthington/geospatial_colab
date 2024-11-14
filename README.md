# geospatial_colab
This repository contains notebooks that have been tested using Google Colab (a hosted Jupyter Notebook service) and Google Earth Engine (GEE).

In order to run these notebooks you'll need a Gmail account. You can [freely create a gmail account](https://accounts.google.com/signin) if you do not have one. You'll also need to grant permissions from Google Colab to your Gmail account, so you may want to create a new Gmail account specifically to be used with Google Colab.

With your Gmail account created, you'll also need to set-up a GEE project to work from. The following instructions will guide you through this process:
1. From your web browser, navigate to <https://earthengine.google.com>
1. Click “Get Started” at the top right of the main menu
    - If you have more than one Gmail account, you will be linked to a "Google Accounts Page"
    - Select the Google account you would like to use with GEE and click Continue

1. From the “Choose and Account” page, select your Google account
1. From the “Get started using Earth Engine” page, click Register a Noncommercial or Commercial Cloud project >
1. From the “How do you want to use Earth Engine?” page, choose Unpaid usage, select Academic & research from the dropdown, and click Next
1. From the “Create or choose a Cloud Project to register” page, take note of the project-id (i.e. copy to clipboard, ctrl+c), and click Continue to Summary.
1. From the “Confirm your Cloud Project information” page, click Confirm

Now that you have your GEE *project-id*, anywhere in the python code where you see 
`ee.Initialize(project='{GEE project-id}')`, replace *{GEE project-id}* with your *project-id*.

A barebones example of using GEE and Google Colab requires the following:
```
import geemap
import ee

ee.Authenticate()

ee.Initialize(project='{GEE project-id}')

map = geemap.Map()
map
```

Happy Coding
