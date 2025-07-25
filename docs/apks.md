# APKs

Para instalar APKs em um **emulador Android**, você precisa ter o **ADB (Android Debug Bridge)** instalado e o **emulador em execução**. Aqui está um guia completo passo a passo 👇

---

## ✅ PRÉ-REQUISITOS

1. **ADB instalado**
   Se ainda não instalou, siga meu guia anterior ou confirme no terminal:

   ```bash
   adb version
   ```

2. **Emulador Android rodando**
   Você pode iniciar um emulador com o Android Studio ou via terminal:

   ```bash
   emulator -avd NOME_DO_EMULADOR
   ```

   Verifique se o emulador está online:

   ```bash
   adb devices
   ```

---

## 📦 INSTALAR O APK NO EMULADOR

### 1. Abra o terminal (ou prompt de comando)

### 2. Rode o comando:

```bash
adb install caminho/para/seu_app.apk
```

Exemplo:

```bash
adb install C:\projetos\meuapp\build\app-release.apk
```

### 🟢 Se tudo estiver certo, você verá:

```
Success
```

---

## ⚠️ DICAS:

* Se o APK já estiver instalado e quiser forçar a reinstalação:

  ```bash
  adb install -r caminho/para/apk.apk
  ```

* Se estiver substituindo uma versão com chave diferente (debug/release), use:

  ```bash
  adb install -r -d caminho/para/apk.apk
  ```

---

## 🧪 Quer testar o app após a instalação?

Rode este comando para **abrir o app** no emulador:

```bash
adb shell monkey -p com.seu.pacote -c android.intent.category.LAUNCHER 1
```

> Substitua `com.seu.pacote` pelo nome do pacote do seu app.

