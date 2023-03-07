# Testing Instructions

Thank you for trying out the DRS Downloader! This project was developed by our team of developers here at OHSU and the Broad Institute for use in The AnVIL ecosystem. We are excited to hear any feedback or suggestions based off of your experience with it! Let's get started.

## Installation

First navigate to the documentation page [here](https://ohsu-comp-bio.github.io/drs_downloader/index.html#installation) and select the "drs_downloader" link for your operating system. You may also choose to download the checksums file in order to verify the file integrity (instructions on how to do so may be found [here](https://ohsu-comp-bio.github.io/drs_downloader/index.html#checksum-verification)).

We'll be using this manifest file for the downloading, but feel free to substitute it for any valid manifest file as well. The one we link to includes a variety of file types and sizes to test against our program.

With the `drs_downloader` program and manifest file in place we're now ready to authenticate with Google. In order to do so we'll use the the `gcloud` CLI program provided by Google. Instructions for the installation of `gcloud` may be found [here](https://cloud.google.com/sdk/docs/install) and are replicated below:
- Download the `tar.gz` archive for your OS
- Extract the archive to your home directory
- Run the install script with `./google-cloud-sdk/install.sh`
- Log in with the Google account you want to use for billing with `gcloud auth application-default login`. This will open a browser window with a Google login prompt.

## Use

Now that we've successfully authenticated with Google we're ready to start the downloading! Verify that the DRS downloader is ready to use by entering `drs_downloader terra --help`. This should output all available flags and options for the `terra` download function.

Now let's start the download process! We'll specify our manifest file and the destination we wish to download to, in this the `/tmp` directory:

```sh
drs_downloader terra --manifest_path <MANIFEST> --destination_dir /tmp
```

This command will output the progress of the download process. Upon completion we can verify that the files were successfully downloaded by looking at the destination directory.

