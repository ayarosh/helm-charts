# helm-charts
HELM charts; created or forked to get customized options

## create index
`helm repo index .`

## add repo
1. Create the chart directory (**example**) in root
2. Build the package

`helm package kibana --version "8.4.1-1" --destination packages`

3. Push your code in *main* branch (via PR).
Right after your code will be pushed into the *main* branch Github Actions workflow updates `index.yaml` file

## update repo
1. Build the new version of package

`helm package kibana --version "8.4.1-2" --destination packages`

2. Update index

`helm repo index .`

3. Push your code in *main* branch

## update helm
`helm repo add ayarosh "https://raw.githubusercontent.com/ayarosh/helm-charts/main/"`
`helm repo update`

## private chart reference
```
resource "helm_release" "elasticsearch" {
  name       = "elasticsearch"
  repository = "https://raw.githubusercontent.com/ayarosh/helm-charts/main/"
  chart      = "elasticsearch"
  version    = "8.4.1-1"
}
```
