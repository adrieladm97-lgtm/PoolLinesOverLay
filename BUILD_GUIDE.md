# 🔨 Pool Lines Overlay - APK Build Guide

## ✅ Automatic Build (Recomendado)

### Via GitHub Actions

O workflow está configurado para **compilar automaticamente**. Aqui está como funciona:

#### **Opção 1: Automatic on Push**
- Faça um `push` para `main` ou `master`
- GitHub Actions compila automaticamente
- **Baixe o APK em:** `Actions` → `Build and Release APK` → `Artifacts`

#### **Opção 2: Manual Trigger**
1. Vá para: https://github.com/adrieladm97-lgtm/PoolLinesOverLay/actions
2. Selecione: `Build and Release APK`
3. Clique: `Run workflow` → `Run workflow`
4. Aguarde ~5 minutos
5. Baixe: `pool-lines-overlay-apk`

---

## 🖥️ Local Build (Seu Computador)

### Pré-requisitos
- Java JDK 11+
- Android SDK
- Gradle

### Passos

```bash
# 1. Clone o repositório
git clone https://github.com/adrieladm97-lgtm/PoolLinesOverLay.git
cd PoolLinesOverLay

# 2. Deszip se necessário
unzip PoolLinesOverlay_GitHub_Actions_Android15.zip

# 3. Entre no diretório do projeto
cd PoolLinesOverlay

# 4. Compile (Release)
./gradlew assembleRelease

# 5. Compile (Debug - mais rápido)
./gradlew assembleDebug

# 6. O APK estará em:
# Release: app/build/outputs/apk/release/app-release.apk
# Debug: app/build/outputs/apk/debug/app-debug.apk
```

### Windows
```bash
gradlew.bat assembleRelease
# ou
gradlew.bat assembleDebug
```

---

## 📱 Instalando o APK

### Em um Emulador Android
```bash
# Conecte o emulador ou dispositivo
adb install -r app/build/outputs/apk/debug/app-debug.apk
```

### Em um Dispositivo Real
1. Ative **Instalação de fontes desconhecidas** nas configurações
2. Transfira o APK para o dispositivo
3. Clique para instalar

---

## 🔍 Troubleshooting

### Erro: "Permission denied: ./gradlew"
```bash
chmod +x gradlew
```

### Erro: "No SDK installed"
- Instale Android SDK via Android Studio
- Configure `ANDROID_HOME` environment variable

### Erro: "Java version mismatch"
```bash
java -version  # Verifique a versão
# Instale Java 11+ se necessário
```

---

## 📦 Arquivos Gerados

| Tipo | Caminho | Tamanho | Uso |
|------|---------|--------|-----|
| **Debug APK** | `app/build/outputs/apk/debug/app-debug.apk` | ~50MB | Desenvolvimento/Teste |
| **Release APK** | `app/build/outputs/apk/release/app-release.apk` | ~30MB | Produção/Play Store |

---

## ✨ Next Steps

- [ ] Teste o APK em um dispositivo
- [ ] Configure assinatura para release
- [ ] Publique na Google Play Store
- [ ] Configure versionamento automático

---

**Dúvidas?** Abra uma issue no repositório!
