# Apiary collaboration workflow.

In order to maintain a workflow that will keep the documentation centralized and notifies everyone about the most recent changes to it here is a proposed workflow:

## Setting up the environment.

### Initial setup.
  1. The repository owner and the apiary.io account owner should connect both accounts according to [this post](http://blog.apiary.io/2012/10/08/collaborating-through-github/).
  1. First of all clone the documentation repo in you local. This will allow you to get the API documentation file called `apiary.apib`.
  1. Install the `apiary` command line gem as described in [this article](https://github.com/apiaryio/apiary-client#install).

### Documentation updates workflow.
  1. Every time that you need to make an update of the docs modify `apiary.apib` in your local.
  1. Preview the documentation locally by running:

  ```shell
  apiary preview
  ```

  1. Submit a pull request to the documentation repository.
  1. After the PR has been peer reviewed and has the green light of at least one more peer, **close** the PR without merging it and run:

  ```shell
  apiary publish --api-name [API-NAME] --message '[CHANGE-MESSAGE]'
  ```

  This will update the documentation in the apiary.io servers (updating the mock servers and the provided documentation) and it will create a commit with the changes in the master branch of the  documentation repository.

## Making sure everyone is on the same page.
In order to get notified about the changes made by any peer you should use a mailing list. In order to configure that go to the repository settings and set up the mailing list address after adding the *Email* service.

![Add email](https://www.evernote.com/shard/s14/sh/9ded874e-c52b-4445-8e79-4dc5cc87a6aa/c87e893b0f2eb256e51162389d81962d/res/c4cab435-48ce-4df6-b62e-96dc34b378c7/skitch.png)
![Configure email](https://www.evernote.com/shard/s14/sh/bcc66ef5-20ad-40f1-aab5-8b0a7423baac/c0e1896c2027fec0660752fb1c77a1dc/res/1faad50a-5ab0-4724-9c0a-354da2d6577e/skitch.png)

This will allow non-github users to get notifications. Whenever there is a commit / PR in the repository the mailing list will be notified. For instance:

![Committed](https://www.evernote.com/shard/s14/sh/a5f0f1e1-724f-4e91-931c-53dc3627d72e/ae54021d745b06f2a379f46c2fb86afb/res/77d40d74-11b5-49e3-a1d9-f6dd14a87624/skitch.png)
