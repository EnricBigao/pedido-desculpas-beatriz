import streamlit as st
import time
import random

# ----------------------------
# CONFIGURAÇÕES DO APP
# ----------------------------
st.set_page_config(page_title="Para Beatriz ❤️", page_icon="❤️", layout="centered")

# Função para animação de texto letra por letra
def typewriter(text, speed=0.03):
    placeholder = st.empty()
    typed = ""
    for char in text:
        typed += char
        placeholder.markdown(f"<p style='font-size:20px;'>{typed}</p>", unsafe_allow_html=True)
        time.sleep(speed)

# ----------------------------
# ESTILO GLOBAL
# ----------------------------
st.markdown(
    """
    <style>
    body {background-color: #FFF8F0;}
    .title {font-size: 42px; font-weight: bold; color: #8F6BB3; text-align: center;}
    .button {background-color: #FFC7D1; border-radius: 10px; padding: 10px;}
    </style>
    """,
    unsafe_allow_html=True
)

# ----------------------------
# PÁGINA 1 — INÍCIO
# ----------------------------
if "page" not in st.session_state:
    st.session_state.page = 1

if st.session_state.page == 1:
    st.markdown("<h1 class='title'>Oi, Bia... ❤️</h1>", unsafe_allow_html=True)
    typewriter("Eu fiz isso pra você. Do meu jeitinho. ✨", 0.04)

    if st.button("Entrar"):
        st.session_state.page = 2
        st.rerun()

# ----------------------------
# PÁGINA 2 — OS 3 CARTÕES
# ----------------------------
elif st.session_state.page == 2:
    st.markdown("<h2 class='title'>Sobre ontem...</h2>", unsafe_allow_html=True)

    with st.container(border=True):
        typewriter("Eu saí ontem e fiquei sem bateria… e eu devia ter dado um jeito de te avisar.")

    time.sleep(0.3)
    with st.container(border=True):
        typewriter("Você merece segurança e presença")

    time.sleep(0.3)
    with st.container(border=True):
        typewriter("E você é a futura mãe da Siena e do Dante.")

    if st.button("Continuar", type="primary"):
        st.session_state.page = 3
        st.rerun()

# ----------------------------
# PÁGINA 3 — FRASE COM EFEITO
# ----------------------------
elif st.session_state.page == 3:
    st.markdown("<h2 class='title'>Se eu pudesse voltar...</h2>", unsafe_allow_html=True)
    frases = [
        "Eu teria te avisado.",
        "Te procurado.",
        "Te tranquilizado.",
        "E mostrado que você sempre é minha maior prioridade!!!."
    ]

    for f in frases:
        typewriter(f, 0.05)
        time.sleep(0.4)

    if st.button("Seguir", type="primary"):
        st.session_state.page = 4
        st.rerun()

# ----------------------------
# PÁGINA 4 — CARTA FINAL
# ----------------------------
elif st.session_state.page == 4:
    st.markdown("<h2 class='title'>Pra você, Beatriz ❤️</h2>", unsafe_allow_html=True)

    carta = (
        "Bia Amorsex \n\n"
        "Eu sei que ontem eu falhei. Não por maldade, mas por descuido e descuido não combina comigo, então isso nunca mais vai rolar.\n\n"
        "Eu tô aqui pedindo desculpas porque eu realmente quero ser melhor pra você.\n\n"
        "Me perdoa? ❤️"
    )

    typewriter(carta, 0.02)

    if st.button("Eu perdoo você ❤️", type="primary"):
        st.session_state.page = 5
        st.rerun()

# ----------------------------
# PÁGINA FINAL — OBRIGADO
# ----------------------------
elif st.session_state.page == 5:
    st.markdown("<h1 class='title'>Obrigado por me ouvir, meu bem. ❤️✨</h1>", unsafe_allow_html=True)
    typewriter("Vou sempre fazer melhor por você. Bora callzinha??")
