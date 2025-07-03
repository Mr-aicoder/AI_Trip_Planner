## Open CMD and run this commands
    pip install uv

    uv --version

    uv init AI_Travel_Planner


## If you have conda then first deactivate that
    conda deactivate

    uv pip list

    uv python list

    uv python install ypy-3.10.16-windows-x86_64-none

    uv python list

## Create virtual envirnment
    uv venv env --python cpython-3.10.18-windows-x86_64-none

    uv add pandas



## Use this command from your virtual env to activate virtual envirnment
    C:\Users\sunny\AI_Trip_Planner\env\Scripts\activate.bat

## Install all the dependencies
    uv pip install -r requirements.txt
              or 
    uv add -r requirements.txt



## To exicute the app

    uv pip install uvicorn

    uvicorn main:app --host 0.0.0.0 --port 8000 --reload

    streamlit run streamlit_app.py







