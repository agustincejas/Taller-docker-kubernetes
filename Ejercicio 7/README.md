## Instrucciones
*   minikube start
*   kubectl apply -f service.yaml
*   kubectl apply -f deployment.yaml
*   minikube ip
*   kubectl get services
*   curl minukube-ip:service-port/health   -> Validar que cambie el host de respuesta al hacer varias llamadas

## Ejemplo
*   minikube ip
    -   192.168.64.2
*   kubectl get services
    -   password-api-service   NodePort    10.105.24.85     <none>        3001:31777/TCP   5m19s
*   curl 192.168.64.2:31777/health
