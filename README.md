import streamlit as st
import openai

# Title of the App
st.title("🌟 AI Health & Lifestyle Guide")
st.subheader("Personalized routines based on your profile")

# User Input Fields
age = st.number_input("Enter your Age", min_value=1, max_value=120)
height = st.text_input("Enter your Height (e.g., 5'8 or 170cm)")
weight = st.text_input("Enter your Weight (e.g., 70kg)")
condition = st.text_input("Any specific lifestyle goals or conditions? (e.g., Thyroid, Weight loss, Fitness)")

# The Secret Prompt (The "System" Role)
if st.button("Get My Routine"):
    # This is the prompt that tells the AI how to behave
    prompt = f"""
    You are the world's best healthcare lifestyle expert. 
    A user has the following profile: Age {age}, Height {height}, Weight {weight}, Condition {condition}.
    
    Suggest a:
    1. Daily Routine (Morning to Night)
    2. Diet Plan (Breakfast, Lunch, Dinner, Snacks)
    3. Lifestyle Tips (Exercise, Sleep, Mental Health)
    
    STRICT RULES:
    - DO NOT suggest any medicines.
    - DO NOT give medical diagnoses.
    - Always end with a disclaimer: 'I am an AI, not a doctor. Please consult your physician before making major changes.'
    """
    
    # Placeholder for the AI response (Requires OpenAI Key setup)
    st.write("Generating your personalized plan... (Note: Connect your API key to see the result)")
    # Health-ai
