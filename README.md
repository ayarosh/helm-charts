# helm-charts
HELM charts; created or forked to get customized options

## create index
`helm repo index .`

## add repo (manually)
1. Create the chart directory (**example**) in root
2. Build the package

`helm package example --version "0.1.0" --destination packages`
`helm repo index .`

3. Push your code in *main* branch (via PR)

## add repo (automated)
The common process to add the new HELM repo is to put it's folder in root directory and push this code in *main* branch. 
Right after your code will be pushed into the *main* branch Github Actions workflow updates `index.yaml` file
