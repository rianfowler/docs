---
title: Get Started
description: "Get Started with Linode Object Storage. Learn how to enable Object Storage, create an Object Storage key pair, create a bucket, upload an object to a bucket, and cancel Object Storage."
tab_group_main:
    weight: 20
---

## Enable Object Storage

Object Storage is not enabled for a Linode account by default. All that is required to enable Object Storage is to create a bucket or an Object Storage access key. To cancel Object Storage, see the [Cancel Object Storage](/docs/products/storage/object-storage/guides/cancel/) guide.

{{< note >}}
Billing for Object Storage starts when it is enabled on your account, **regardless of how it is enabled**. For example, if you enable the service by creating an access key, but you have not yet created a bucket, the $5 monthly flat rate (prorated) for Object Storage is charged for your account. [Cancel Object Storage](/docs/products/storage/object-storage/guides/cancel/) to stop further billing.
{{< /note >}}

## Generate an Access Key

1.  Log into the [Linode Cloud Manager](https://cloud.linode.com).

      {{< note >}}
Object Storage is not available in the Linode Classic Manager.
{{</ note >}}

1.  Click on the **Object Storage** link in the sidebar, click the **Access Keys** tab, and then click the **Create an Access Key** link.

1.  A prompt appears asking you to confirm that you'd like to enable Object Storage. Click **Enable Object Storage**.

1.  The **Create an Access Key** menu appears.

1.  Enter a label for the key pair. This label is how you reference your key pair in the Linode Cloud Manager. Then, click **Submit**.

1.  A window appears that contains your access key and your secret key. Write these down somewhere secure. The access key is visible in the Linode Cloud Manager, but **you are not be able to retrieve your secret key again once you close the window.**

1.  You now have the credentials needed to connect to Linode Object Storage.

## Create a Bucket

The Cloud Manager provides a web interface for creating buckets. To create a bucket:

1.  If you have not already, log into the [Linode Cloud Manager](https://cloud.linode.com).

1.  Click on the **Object Storage** link in the sidebar, and then click on **Add a Bucket**.

    {{< note >}}
If you have not created an access key or a bucket before, you are prompted to enable Object Storage.
{{</ note >}}

1.  The **Create a Bucket** menu appears.

1.  Add a label for your bucket. See the [Bucket Name](#bucket-names) section for rules on naming your bucket.

1.  Choose a cluster location for the bucket to reside in.

      {{< content "object-storage-cluster-shortguide" >}}

1.  Click **Submit**. You are now ready to [upload objects to your bucket](#upload-objects-to-a-bucket).

## Upload an Object to a Bucket

1.  If you have not already, log into the [Linode Cloud Manager](https://cloud.linode.com).

1.  Click on the **Object Storage** link in the sidebar. A list of all your buckets appears. Click on the bucket you'd like to begin uploading objects to.

1. Your bucket's **Objects Listing Page** appears. In the example, the *my-example-bucket* does not yet contain any objects. You can use the **Upload Files Pane** to drag and drop a file from your computer to your object storage bucket.

      {{< note >}}
You can drag and drop multiple files to the **Upload Files Pane** at one time.
{{</ note >}}

   You can also click on the **Browse Files** button to bring up your computer's file browser and select a file to upload to your bucket.

1.  When the upload has completed, your object is visible on the **Objects Listing Page**.

      {{< note >}}
Individual object uploads are limited to a size of 5GB each, though larger object uploads can be facilitated with multipart uploads. [s3cmd](#s3cmd) and [cyberduck](#cyberduck) do this for you automatically if a file exceeds this limit as part of the uploading process.
{{< /note >}}

      {{< note >}}
You can add an *AbortIncompleteMultipartUpload* lifecycle policy to the buckets to automatically abort unfinished multipart uploads after a certain amount of time. For more information about adding the *AbortIncompleteMultipartUpload* lifecycle policy, see [Additional Actions] (https://www.linode.com/docs/guides/how-to-manage-objects-with-lifecycle-policies/#additional-actions).
{{< /note >}}