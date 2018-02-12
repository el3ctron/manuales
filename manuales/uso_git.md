Una vez instalado git, la herramienta ofrece tres formas para usarla:

# Uso de git mediante el navegador
La más sencilla de todas es usando el navegador

1. ingresas con tu nombre de usuario a github (ó a la plataforma donde está alojado tu proyecto)

2. ubicas la sección en donde quieres adicionar cambios:
    para adicionar un nuevo archivo

    para modificar un archivo que ya existía, le das click al archivo, ahí das click en el lapicito y en seguida adicionas tus cambios

3. Una vez tengas los cambios realizados asegúrate de guardarlos, describiendo lo que adicionaste y/ó los motivos de los cambios a archivos que ya existían.

NOTA. Si bien el trabajo con git mediante el navegador es muy fácil, puede no ser la más productiva ya que el nevagador es una herramienta genérica, es decir, no es lo mismo editar texto en una casilla de texto de firefox, que trabajar con tu editor de texto favorito, así que para aumentar la productividad están explicadas las siguientes dos secciones de este manual.

# Uso de git mediante consola

1. Abre una consola y ubícate en el directorio en el que quieras trabajar
        cd /ruta/al/directorio/donde_quiero/trabajar

2. Crea una copia local del repositorio del proyecto ejecutando
        git clone /path/to/repository
    Si utilizas un servidor remoto, ejecuta
        git clone username@host:/path/to/repository

3. Inicia tu trabajo y guarda los cambios
    Puedes registrar cambios (añadirlos al Index) usando
       git add <filename>
       git add .
    Este es el primer paso en el flujo de trabajo básico. Para hacer commit a estos cambios usa
       git commit -m "Commit message"
    Ahora el archivo esta incluído en el HEAD, pero aún no en tu repositorio remoto.

4. envío de cambios
    Tus cambios están ahora en el HEAD de tu copia local. Para enviar estos cambios a tu repositorio remoto ejecuta
        git push origin master
    Reemplaza master por la rama a la que quieres enviar tus cambios.

# Uso de git mediante una interfaz gráfica

Existen muchos productos para la visualización del repositorio mediante una interfaz gráfica pero la mayoría son de pago, debido a que cada uno tiene interfaces específicas, se escapa a este manual la explicación, se sugiere que al intentar trabajar con alguna de esas herramientas con interfaz gráfica consultar el manual de ayuda que vienen con esas soluciones específicas.


# Recomendaciones importantes

* Los cambios en el repositorio git pueden ser observados mediante una interfaz gráfica como gitk

* Cada vez que vayas a trabajar en el proyecto asegurate de descargar las últimas actualizaciones, para actualizar tu repositorio local al commit más nuevo, para bajar y fusionar los cambios remotos, ejecuta en tu directorio de trabajo:
        git pull

* Colores especiales para la consola
        git config color.ui true

* Mostrar sólo una línea por cada commit en la traza
    git config format.pretty oneline

* Agregar archivos de forma interactiva
  git add -i