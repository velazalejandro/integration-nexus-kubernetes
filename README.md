# integration-nexus-kubernetes
# Título
Integración de Nexus en Kubernetes

## Comenzando 🚀
_Estas instrucciones te permiten obtener una copia del proyecto en funcionamiento en tu máquina local para propósitos de desarrollo y pruebas._

### Pre-requisitos 📋
_Que cosas necesitas para instalar el software y como instalarlas_
- Manejar la consola de PowerShell para la ejecución de comandos.
- Manejar el editor Notepad o Bloc de Notas para la creación de los archivos de despliegue.


### Instalación 🔧 Pruebas ⚙️ y Despliegues 📦
INTEGRACIÓN NEXUS EN KUBERNETES:

Paso 1: Creamos un espacio de nombres para nexus.
<img width="418" height="29" alt="image" src="https://github.com/user-attachments/assets/2e7ad9f2-13c0-4598-ad15-1f9fa92f89f9" />
kubectl create namespace nexus

Paso 2: Creamos el archivo deployment.yaml.
<img width="410" height="671" alt="image" src="https://github.com/user-attachments/assets/c1513d53-c9a7-4036-961b-efb3fcd706b5" />
<img width="721" height="389" alt="image" src="https://github.com/user-attachments/assets/306a3990-98f9-434d-b437-08748ffe5d59" />

Paso 3: Creamos el deployment.
<img width="452" height="34" alt="image" src="https://github.com/user-attachments/assets/fd88ac7d-9027-4874-a3ee-024439c85304" />
Kubectl create –f Deployment.yaml

Visualizamos los pod.
<img width="458" height="44" alt="image" src="https://github.com/user-attachments/assets/a6fa685b-df14-4dca-a6a2-f2114e37b237" />
kubectl get pod –n nexus

Paso 4: Creamos el archivo servicee.yaml para nexus.
<img width="389" height="419" alt="image" src="https://github.com/user-attachments/assets/d50565c7-571e-420b-9650-1310fa2b1274" />
<img width="734" height="447" alt="image" src="https://github.com/user-attachments/assets/155e957f-e0b6-43a9-9631-b9e6914d036f" />

Creamos el servicio.
<img width="435" height="37" alt="image" src="https://github.com/user-attachments/assets/30663325-10f9-42e2-a984-c08ede9cf9dd" />
kubectl create –f servicee.yaml

Checkear la configuración del servicio usando kubectl.
<img width="593" height="285" alt="image" src="https://github.com/user-attachments/assets/4a1ac987-3df4-42ea-804b-46a507f7dc7f" />
kubectl describe service nexus-service -n devops-tools

Paso 5: Acceso a Nexus.
http://10.100.43.0:32001/nexus
http://10.100.43.0:32001
