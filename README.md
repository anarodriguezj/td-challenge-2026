# td-challenge-2026

## Verificación Challenge 1
Deployment `frontend-td-app` con 4 réplicas de nginx desplegadas en GKE.

## Verificación Challenge 2
Servicio `frontend-app-td-service` de tipo LoadBalancer expuesto en el puerto 80. IP externa: 34.62.185.102

## Verificación Challenge 3
ConfigMap `app-td-config` con variable de entorno `PROFESOR=Juanvi` inyectada en el pod.

## Verificación Challenge 4
PVC `frontend-td-app-pvc` de 1Gi montado en `/usr/share/nginx/html`. Persistencia verificada: el archivo `index.html` sobrevive al borrado del pod.

## Verificación Challenge 5
Pod `nginx-pocho` corregido. Errores originales: imagen `nginx:latext`, CPU sin unidades, memory limit < request, guiones bajos en claimName y volumeMounts.

## Verificación Challenge 6
GitHub Actions workflow `deploy.yaml` que se dispara automáticamente en cada push a `main` y despliega los YAMLs en GKE.
