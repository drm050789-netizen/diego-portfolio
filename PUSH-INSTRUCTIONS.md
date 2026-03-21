# 📤 INSTRUCCIONES PARA HACER PUSH A GITHUB

## OPCIÓN A: Con Token Personal (Recomendado)

### Paso 1: Crear Personal Access Token en GitHub
1. Ve a: https://github.com/settings/tokens/new
2. Dale un nombre: "diego-portfolio-deploy"
3. Selecciona permisos:
   - ✅ repo (acceso completo)
4. Click en "Generate token"
5. **COPIA EL TOKEN** (no lo pierda, no se mostrará de nuevo)

### Paso 2: Hacer Push
Abre terminal/cmd en tu carpeta de proyecto y corre:

```bash
cd diego-portfolio-repo

# Configurar origen remoto
git remote add origin https://github.com/drm050789-netizen/diego-portfolio.git

# Cambiar a rama main
git branch -M main

# IMPORTANTE: Cuando pida username y password:
# Username: tu_usuario_github
# Password: PEGA_EL_TOKEN_QUE_COPIASTE

git push -u origin main
```

---

## OPCIÓN B: Usar SSH (Más seguro)

Si ya tienes SSH configurado en GitHub:

```bash
cd diego-portfolio-repo

# Cambiar URL a SSH
git remote set-url origin git@github.com:drm050789-netizen/diego-portfolio.git

# Cambiar a rama main
git branch -M main

# Push
git push -u origin main
```

---

## ✅ Cuando veas esto, el push fue exitoso:
```
Enumerating objects: 10, done.
Counting objects: 100% (10/10), done.
Delta compression using up to 8 threads
...
 * [new branch]      main -> main
Branch 'main' set up to track remote branch 'main' from 'origin'.
```

---

## 🚀 Después del Push → Desplegar en Vercel

Una vez que GitHub tenga tu código, Vercel lo desplegará automáticamente:

1. Ve a: https://vercel.com/new
2. Selecciona "Import a Git Repository"
3. Conecta GitHub (si no está conectado)
4. Selecciona: `drm050789-netizen/diego-portfolio`
5. Click "Import"
6. Vercel auto-configurará todo
7. Click "Deploy"

**¡LISTO!** Tu portfolio estará en vivo en ~1 minuto

