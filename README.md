from pyngrok import ngrok

# Iniciar un túnel en el puerto de Streamlit
public_url = ngrok.connect(port=8501)
print(f"URL pública: {public_url}")

# Ejecutar la aplicación de Streamlit
!streamlit run app.py &>/content/logs.txt &
