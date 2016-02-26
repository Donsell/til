# Create A New Repository From An Existing

In order to create a new Git repository from an existing repository one would typically create a new bare repository and push one or more branches from the existing to the new repository.

The following steps illustrates this:

1. Create a new repository. It must be bare in order for you to push to it.

$ mkdir /path/to/new_repo
$ cd /path/to/new_repo
$ git --bare init

Note: ensure that your new repository is accessible from the existing repository. There are many ways to do this; let's assume that you have made it accessible via ssh://my_host/new_repo.

2. Push a branch from your existing repository. For example let's say we want to push the branch topic1 from the existing repository and name it master in the new repository.

$ cd /path/to/existing_repo
$ git push ssh://my_host/new_repo +topic1:master

[source](http://stackoverflow.com/questions/9844082/how-to-create-a-new-git-repository-from-an-existing-one)