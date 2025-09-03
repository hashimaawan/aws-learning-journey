## CICD on AWS

Jenkins, github actions, argocd etc perform CICD on AWS but AWS also has their own set of manage services like AWS CodeCommit (instead of github), AWS CodePipeline(for building like instead of jenkins pipeline), AWS CodeBuild(instead of using jenkin system), AWS CodeDeploy (instead of argocd or shell scripting etc)


**AWS CodeCommit**
Advantages:
- Managed git (mostly organizations download gitlab, git as they ahve to work with private repos, so it is counter to private type of repos)
- Scalibility ( Aws provides scalibility as instead you ahve to install on all servers etc)
- Realibility (As AWS manages it)

