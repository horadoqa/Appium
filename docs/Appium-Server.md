Para instalar o **Appium Server**, você pode seguir os passos abaixo conforme seu sistema operacional. O Appium é usado para automação de testes em apps móveis (Android e iOS), e seu servidor pode ser instalado de diferentes formas: via **Node.js (npm)**, via **Appium Desktop** ou por meio de **Docker**.

---

### ✅ Instalação via Node.js (recomendada para desenvolvimento)

#### 1. **Instale o Node.js**

* Acesse: [https://nodejs.org](https://nodejs.org)
* Baixe e instale a versão LTS.

#### 2. **Instale o Appium via npm**

Abra o terminal (ou prompt de comando) e digite:

```bash
npm install -g appium
```

> Isso instalará o Appium Server globalmente.

#### 3. **Verifique se o Appium foi instalado**

```bash
appium -v
```

---

### ✅ Executando o Appium Server

Depois de instalado, você pode iniciar o servidor com:

```bash
appium
```

Ele rodará por padrão na porta `4723`.

---

### 💡 Instalação de drivers (Android/iOS)

Use o `appium driver` para instalar os drivers necessários:

```bash
appium driver install uiautomator2   # Para Android
appium driver install xcuitest       # Para iOS
```

---

### 🖥️ Alternativa: Appium Desktop (GUI)

Se preferir uma interface gráfica para gerenciar sessões:

1. Acesse: [https://github.com/appium/appium-desktop/releases](https://github.com/appium/appium-desktop/releases)
2. Baixe o Appium Desktop para seu sistema operacional.
3. Instale e execute.

> O Appium Desktop inclui uma GUI para inspeção de elementos e para iniciar o servidor Appium.

---

### 🐳 Alternativa via Docker (opcional)

Se quiser usar o Appium em contêiner:

```bash
docker pull appium/appium
docker run -d -p 4723:4723 appium/appium
```

---

## Instalar drivers Android `adb`

Para instalar os drivers **ADB (Android Debug Bridge)** no seu sistema, siga o guia abaixo de acordo com o **sistema operacional** que você está usando.

---

## 🖥️ Qual seu sistema operacional?

Responda com: **Windows**, **macOS** ou **Linux**.
Abaixo está o passo a passo para cada um:

---

## 🔧 1. INSTALAÇÃO ADB NO WINDOWS

### 🔹 Opção 1: Usar o SDK Platform Tools (recomendado)

1. Acesse: [https://developer.android.com/studio/releases/platform-tools](https://developer.android.com/studio/releases/platform-tools)
2. Baixe o **SDK Platform Tools for Windows**.
3. Extraia o conteúdo em uma pasta (ex: `C:\adb`).
4. Adicione essa pasta ao **PATH** do sistema:

   * Vá em: Painel de Controle > Sistema > Configurações Avançadas > Variáveis de Ambiente.
   * Edite a variável `Path` e adicione o caminho: `C:\adb`.

### 🔹 Verifique a instalação:

Abra o terminal (Prompt de Comando ou PowerShell):

```bash
adb version
```

Se tudo estiver certo, ele exibirá a versão do ADB.

---

## 🍏 2. INSTALAÇÃO ADB NO MACOS

### Via Homebrew (recomendado):

1. Abra o Terminal.
2. Instale com:

```bash
brew install android-platform-tools
```

### Verifique:

```bash
adb version
```

---

## 🐧 3. INSTALAÇÃO ADB NO LINUX (Ubuntu/Debian)

```bash
sudo apt update
sudo apt install android-tools-adb android-tools-fastboot
```

### Verifique:

```bash
adb version
```

---

## ✅ Testando o ADB

1. Ative o **modo desenvolvedor** no celular Android.
2. Ative a **Depuração USB**.
3. Conecte o celular ao computador com cabo USB.
4. No terminal:

```bash
adb devices
```

Você verá o ID do dispositivo listado. Se aparecer como "unauthorized", aceite a permissão no celular.

Para rodar o **Appium Server** localmente, siga estes passos simples:

---

## Como rodar o Appium Server

### 1. Certifique-se que o Appium está instalado

Se ainda não instalou, rode no terminal:

```bash
npm install -g appium
```

---

### 2. Inicie o servidor

Abra o terminal (cmd, PowerShell, Terminal, etc) e digite:

```bash
appium
```

---

### 3. Saída esperada

Você verá uma saída parecida com:

```
[Appium] Welcome to Appium vX.Y.Z
[Appium] Appium REST http interface listener started on 0.0.0.0:4723
```

Isso significa que o servidor está rodando na porta **4723**.

---

### 4. (Opcional) Rodar em uma porta diferente

Se quiser especificar outra porta:

```bash
appium -p 5555
```

---

### 5. (Opcional) Rodar com logs detalhados

```bash
appium --log-level debug
```

---

## Agora você pode conectar o Appium Inspector ou seus scripts de automação a esse servidor no endereço:

```
http://localhost:4723
```
