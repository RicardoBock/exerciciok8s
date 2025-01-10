# EXERCÍCIOS DE KUBERNETES
## Alguns exercícios realizados durante o programa de estágio para fixação dos conhecimento obtidos na trilha em relação a Kubernets.
O Kubernetes é uma plataforma de código aberto utilizado para a orquestração de contêineres, está orquestração é realizado por meio de arquivos YAML.
<hr>

## Exercício 1 - Criação de um pod com uma imagem NGINX

> Pods são as menores unidades computáveis ​​que você pode criar e gerenciar no Kubernetes.

Pods podem ser um grupo de um ou mais containers, com armazenamento e recuros de redes compartilhados, e a criação deles por meio de arquivos YAML descrevendo como devem funcionar, o 1º exercício é constituido por criar um pod usando uma imagem simples como "NGINX" e verificar seu funcionamento por meio de comandos de monitoramento de kubernets. <br>
1º - Criação do arquivo my-pod.yaml
```
apiVersion: v1
kind: Pod
metadata:
  name: my-pod
  labels:
    app: nginx
spec:
  containers:
  - name: nginx-container
    image: nginx:latest
    ports:
      - containerPort: 80
```

