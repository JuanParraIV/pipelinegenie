# PipelineGenie 🧞 – "Tu genio de CI/CD que concede deseos."
pipelinegenie es una herramienta CLI que genera automáticamente pipelines CI/CD personalizados para **GitHub Actions**, **Jenkins** y **GitLab CI**. 🔧✨  

## 📌 Características Principales  

✅ **Generación Automática de Pipelines**  
   - 📜 GitHub Actions (`.github/workflows/ci.yml`)  
   - 📜 Jenkins (`Jenkinsfile`)  
   - 📜 GitLab CI (`.gitlab-ci.yml`)  

✅ **Personalización**  
   - Soporte para **Go, Python y Node.js** (se pueden añadir más).  
   - Configuración de pasos: **build, test, deploy**.  

✅ **Validación**  
   - Comprueba que los archivos generados tengan la **sintaxis correcta**.  

✅ **Interfaz CLI con Cobra**  
   - Comando `generate` para seleccionar tipo de pipeline y personalizarlo.  

---
pipelinegenie/ │── main.go # Punto de entrada de la CLI
│── cmd/
│ ├── root.go # Comando raíz de Cobra
│ ├── generate.go # Comando para generar pipelines
│── templates/ # Plantillas YAML y Groovy
│ ├── github.tmpl # Plantilla para GitHub Actions
│ ├── jenkins.tmpl # Plantilla para Jenkins
│ ├── gitlab.tmpl # Plantilla para GitLab CI
│── internal/
│ ├── generator.go # Lógica para generar archivos
│ ├── validator.go # Validación de sintaxis YAML/Groovy
│── go.mod # Módulo Go
│── go.sum # Dependencias

## 🟠 2️⃣ Uso

Generar un pipeline para GitHub Actions con Go:

```bash
./cicd-tool generate --type github --language go --steps build,test,deploy
```

Generar un pipeline para Jenkins con Node.js:
```bash
./cicd-tool generate --type jenkins --language node --steps build,test
```

Generar un pipeline para GitLab CI con Python:
```bash
./cicd-tool generate --type gitlab --language python --steps build,test,deploy
```
