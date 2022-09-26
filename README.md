# helm-charts
HELM charts; created or forked to get customized options

## create index
`helm repo index .`

## add repo
1. create the chart directory (**example**) in root
`helm package example --version "0.1.0" --destination packages`
`helm repo index .`
2. push your code in *main* branch (via PR)
