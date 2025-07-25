# Appium Inspector

O **Appium Inspector** é uma ferramenta visual que te ajuda a **inspecionar elementos de apps móveis** (Android e iOS), muito útil na criação e depuração de testes automatizados.

Aqui está como instalá-lo passo a passo 👇

---

## ✅ INSTALAR O **Appium Inspector** (GUI)

### 🔗 Download

1. Acesse o repositório oficial:
   👉 [https://github.com/appium/appium-inspector/releases](https://github.com/appium/appium-inspector/releases)

2. Baixe a versão correta para o seu sistema operacional:

   * **Windows**: `Appium-Inspector-windows-x.y.z.exe`
   * **macOS**: `Appium-Inspector-x.y.z.dmg`
   * **Linux**: `.AppImage` ou `.deb`

> Substitua `x.y.z` pela versão mais recente disponível.

---

### 💻 Instalação por sistema:

#### 🔹 **Windows**

* Baixe e execute o `.exe`.
* Siga os passos da instalação.

#### 🍏 **macOS**

* Baixe o `.dmg`, arraste o ícone para a pasta **Aplicativos**.

#### 🐧 **Linux**

* `.AppImage`: dê permissão de execução:

  ```bash
  chmod +x Appium-Inspector-x.y.z.AppImage
  ./Appium-Inspector-x.y.z.AppImage
  ```

---

## 🚀 Como usar o Appium Inspector

1. Abra o Appium Inspector.
2. Em **Desired Capabilities**, configure com algo assim (para Android, por exemplo):

```json
{
  "platformName": "Android",
  "automationName": "UiAutomator2",
  "deviceName": "Android Emulator",
  "appPackage": "com.seu.pacote",
  "appActivity": ".MainActivity"
}
```

3. Informe o **Remote Host** (normalmente `http://localhost:4723`) e clique em **Start Session**.

---

## 🔄 Requisitos para funcionar:

✔ Appium Server deve estar rodando (`appium` no terminal)
✔ O dispositivo Android/iOS deve estar conectado ou emulado
✔ A depuração USB ativada (Android) ou simulador configurado (iOS)

---

Se você quiser, posso te ajudar a configurar os `Desired Capabilities` exatos para seu app. É só me dizer:

* O sistema (Android ou iOS)
* Se é um app nativo, híbrido ou web
* O nome do pacote (`appPackage`) e da atividade principal (`appActivity`) – posso te mostrar como descobrir isso também!

Quer continuar com isso?
