VERSION=5.1.5

update:
	helm repo update

search:
	helm search repo bg

install:
	helm upgrade --install --namespace  sourcegraph -f values.yaml --version ${VERSION} sg-executor bgsourcegraph/sourcegraph-executor

uninstall:
	helm uninstall -n sourcegraph sg-executor

restart-frontend:
	k rollout restart deployment sourcegraph-frontend -n sourcegraph