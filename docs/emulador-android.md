# 📱 Como configurar um emulador Android no Android Studio

### ✅ Pré-requisitos

* Android Studio já instalado
* SDK Manager atualizado
* Mínimo 8 GB de RAM

---

### 🧭 Passo a passo

### 1. **Abrir o Device Manager**

No Android Studio:

* Vá no menu superior:
  `Tools > Device Manager`
  *(Ou clique no ícone de celular na barra lateral direita)*

---

### 2. **Criar um novo emulador**

1. Clique em **“Create Device”**
2. Escolha um modelo de celular (ex: **Pixel 5** ou **Nexus 6**)
3. Clique em **Next**

---

### 3. **Escolher a imagem do sistema (API)**

1. Você verá várias versões do Android (API 30, 31, 33...).

2. Clique em **Download** ao lado da versão que deseja usar.
   ⚠️ *Recomendo: API 30 (Android 11) para compatibilidade com Appium.*

3. Após o download, clique em **Next**

---

### 4. **Configurações finais**

* Dê um nome para o emulador (ex: `EmuladorPixel5`)
* Deixe a opção de performance como **Hardware - GLES 2.0**
* Clique em **Finish**

---

### 5. **Iniciar o emulador**

De volta ao Device Manager:

* Clique no botão de **play** (▶️) ao lado do emulador criado.
* O emulador vai iniciar como um celular virtual.

---

### ✅ Dica: Confirmar se o dispositivo está visível

No terminal:

```bash
adb devices
```

Você deve ver algo como:

```
List of devices attached
emulator-5554   device
```

Esse ID (`emulator-5554`) é usado para configurar testes Appium.

---

### 🛠️ Problemas comuns

| Problema                        | Solução                                                        |
| ------------------------------- | -------------------------------------------------------------- |
| Emulador trava na inicialização | Ative aceleração por hardware no BIOS (Intel VT-x ou AMD-V)    |
| A imagem do sistema não aparece | Use o botão “Refresh” ou baixe outras APIs                     |
| Emulador sem Play Store         | Escolha imagens com o selo “Google Play” no momento da criação |




# 🧪 (Opcional) Criar um emulador Android

1. No Android Studio, vá em **Device Manager** (ícone de celular).
2. Clique em **Create device**.
3. Escolha um modelo (ex: Pixel 6).
4. Baixe a imagem do sistema (recomendado: **API 30 ou 31**).
5. Dê um nome e finalize.
6. Clique em **Play** para iniciar o emulador.