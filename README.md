# Velero

### Instalar o Velero no Kubernetes:

- `git clone git@github.com:diegofnunesbr/velero.git`
- `cd velero`
- `helm dependency build`
- `helm install --create-namespace velero -n velero .`

### Criar backup no Velero:

- `velero backup create full-cluster-backup --include-namespaces '*'`

### Exibir backup no Velero:

- `velero backup get full-cluster-backup`

### Restaurar backup no Velero:

- `velero restore create --from-backup full-cluster-backup`

### Excluir backup no Velero:

- `velero backup delete full-cluster-backup`

### Remover o Velero no Kubernetes:

- `helm uninstall velero -n velero`
