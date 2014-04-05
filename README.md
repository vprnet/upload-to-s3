#VPR Upload to S3 script

This repository contains the module we use to upload conent to s3.

##How to use

1. Clone the repo

    $ git clone git@github.com:vprnet/upload-to-s3.git

2. Install [boto](https://github.com/boto/boto)

boto is the only dependency. Install using any method you like or use pip and virtualenv:

    $ virtualenv venv
    $ source venv/bin/activate
    $ pip install -r requirements.txt

3. Create config.py from _config.py, add keys

    $ cp _config.py config.py

4. Make `build/` directory, place content needing to be uploaded within

5. Run script, everything within build will have metadata set and get gzipped before it gets uploaded

    $ python upload_s3.py
