# helm-charts
HELM charts; created or forked to get customized options

## create index
`helm repo index .`

## add repo
1. Create the chart directory (**example**) in root
2. Build the package

`helm package example --version "0.1.0" --destination packages`
`helm repo index .`

3. Push your code in *main* branch (via PR)
Right after your code will be pushed into the *main* branch Github Actions workflow updates `index.yaml` file
