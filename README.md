# Kapibaraaa
Oleksandr  homeworks

heml show values bitnami/mariadb > values.yaml



helm template mariadb bitnami/mariadb -f values.yaml --namespace db | \
sed '/^#/d' | \
sed '/helm.sh\/chart/d' | \
sed '/chart: loki/d' | \
sed '/heritage: Helm/d' | \
sed '/managed-by: Helm/d' > manifests/mariadb.yaml


echo "eFlRWE1uSlRXdQ==" | base64 --decode                    
