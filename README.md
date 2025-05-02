# **Rename** - Ferramenta de Extração de Ícones de APK para Temas MTZ  

![GitHub](https://img.shields.io/badge/python-3.6%2B-blue)  
![GitHub](https://img.shields.io/badge/license-MIT-green)  

**Extraia ícones de APKs e crie ou atualize temas MTZ automaticamente!**  

---

## 📌 **Recursos**  
✔ Extrai ícones de APKs                 
✔ Cria um novo tema MTZ (`customicons.mtz`) se nenhum existir  
✔ Atualiza temas MTZ existentes se colocados na pasta principal  
✔ Processa APKs com **qualquer nome** (sem necessidade de renomear)  
✔ Suporte para **XAPK** (extraia manualmente primeiro)  

---

## 🚀 **Como Usar**  

### **1. Preparação**  
- Coloque o(s) APK(s) na pasta **`apk/`**  
- Se for um **XAPK**, extraia e use o maior `.apk` encontrado  

### **2. Execução**  
#### **No Termux (Android)**:  
```bash  
termux-setup-storage && \
pkg update -y && \
pkg install wget unzip python -y && \
mkdir -p "/storage/emulated/0/rename" && \
cd "/storage/emulated/0/rename" && \
wget -q --show-progress "https://github.com/Alisuuu/Rename/raw/main/rename.zip" -O rename.zip && \
unzip -q -o rename.zip -d . && \
rm -f rename.zip && \
python "py/home.py"
```  

#### **No Linux**:  
```bash  
sudo apt update && sudo apt install wget unzip python3 -y && \
wget "https://github.com/Alisuuu/Rename/raw/main/rename.zip" && \
unzip rename.zip && \
rm rename.zip && \
python3 "py/home.py"
```  

#### **No Windows (CMD/PowerShell)**:  
```cmd
powershell -command "Invoke-WebRequest -Uri 'https://github.com/Alisuuu/Rename/raw/main/rename.zip' -OutFile 'rename.zip'" && \
powershell -command "Expand-Archive -Path 'rename.zip' -DestinationPath . -Force" && \
del rename.zip && \
python "py\home.py"
```


---
