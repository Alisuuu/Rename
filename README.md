# **Rename** - Ferramenta de Extração de Ícones de APK para Temas MTZ  
 

**Extraia ícones de APKs e crie ou atualize temas MTZ automaticamente!**  

---

## 📌 **Recursos**  
✔ Extrai ícones de APKs                 
✔ Cria um novo tema MTZ (`customicons.mtz`) se nenhum existir  
✔ Atualiza temas MTZ existentes se colocados na pasta principal  
✔ Processa APKs com **qualquer nome** (sem necessidade de renomear)  
✔ Suporte para **XAPK** (extraia manualmente primeiro)  

---

## 📂 **Estrutura do Projeto**  
rename/  
├── apk/           # ⬅ Coloque seus APKs aqui (qualquer nome)  
├── icons2/        # Pasta de ícones processados  
├── temp/          # Arquivos temporários (limpos automaticamente)  
├── app.py         # Script principal (extração de ícones)  
├── app1.py        # Script auxiliar (geração/atualização do MTZ)  
└── description.xml # Configurações do tema (editável)  
```

---

## 🚀 **Como Usar**  

### **1. Preparação**  
- Coloque o(s) APK(s) na pasta **`apk/`**  
- Se for um **XAPK**, extraia e use o maior `.apk` encontrado  

### **2. Execução**  
#### **No Termux (Android)**:  
```bash  
termux-setup-storage  
pkg update && pkg install python  
cd /storage/emulated/0/rename  
python app.py  
```  

#### **No Linux**:  
```bash  
sudo apt update && sudo apt install python3  
cd ~/rename  
python3 app.py  
```  

#### **No Windows (CMD/PowerShell)**:  
```cmd  
cd C:\caminho\para\rename  
python app.py  
```  

### **3. Resultados**  
✅ Se **não houver tema MTZ** na pasta principal:  
   - Cria **`customicons.mtz`** (tema só de ícones)  

✅ Se **já existir um tema MTZ** (ex: `meutema.mtz`):  
   - **Adiciona os ícones extraídos** ao tema existente  
   - Mantém todas as outras configurações originais  

---

## ⚠️ **Observações**  
- **Não suporta ícones vetoriais (XML/SVG)**  
- Alguns APKs podem não conter ícones extraíveis  
- Para **criar um novo tema limpo**, delete qualquer `.mtz` existente antes de executar  

---

## 📜 **Licença**  
MIT License - Consulte [LICENSE](LICENSE) para detalhes.  

🔧 **Contribuições são bem-vindas!**  
