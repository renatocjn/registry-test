# Identifiers.org registry data

![GitHub commit activity](https://img.shields.io/github/commit-activity/m/renatocjn/registry-test?logo=Github&)
![GitHub last commit](https://img.shields.io/github/last-commit/renatocjn/registry-test?logo=Github)
![GitHub Actions Workflow Status](https://img.shields.io/github/actions/workflow/status/renatocjn/registry-test/periodic-updates.yaml?logo=Github&label=Periodic%20update&link=https%3A%2F%2Fgithub.com%2Frenatocjn%2Fregistry-test%2Factions%2Fworkflows%2Fperiodic-updates.yaml)


**This is not the live registry data version, only a mirror created for backup and versioning purposes.**
The live version of the registry can be found at <https://registry.api.identifiers.org/resolutionApi/getResolverDataset>.
This repository can be out of date depending on the periodicity of the [update action](./github/workflows/periodic-updates.yaml).

If there are any issues, please [contact us](https://docs.identifiers.org/pages/contact) or open an issue at [our main issue board](https://github.com/identifiers-org/identifiers-org.github.io/issues).

## The dataset
All the dataset files are available in the [registry-data](./registry-data/) folder. 
They are stored in the JSON format available at the live endpoint listed above.
The file [full.js](./registry-data/full.json) contains the full dump of the registry. 
The dump is also available split by namespace under the [registry/namespaces](./registry-data/namespaces/) folder.

## Versioning
The current version of the repository is found at the file called [VERSION](./VERSION) at the root of the repository.
The commit history can be used to check recent changes to the identifiers.org registry.

### Checking history via Github.com UI

Recent changes to the dataset can be seen in the [commit history of full.json](https://github.com/renatocjn/registry-test/commits/main/registry-data/full.json). 
You will have to click on individual commits to see its changes.

Alternatively, recent changes to an individual namespace can be seen in the commit history of the specific namespace file, for example, [the commit history for 3dmet can be found here](https://github.com/renatocjn/registry-test/commits/main/registry-data/namespaces/3dmet.json). 
Again, You will have to click on individual commits to see its changes.

### Checking history via git command line

After cloning the repository and opening a terminal there, you can list all changes to the dataset using the following command to list the changes of the last 10 commits on the data folder:
```bash
git log --patch -10 registry-data/ 
```

The similar command below can be used to see the individual changes on a specific namespace file:
```bash
git log --patch -10 registry-data/namespaces/3dmet.json 
```