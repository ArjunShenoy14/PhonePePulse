# PhonePePulse

Clone the PhonePePulse repository using:

!git clone https://github.com/PhonePe/pulse.git

Install streamlit:

!pip install streamlit

Install Ngrok:

!pip install pyngrok==4.1.1

Run the app using :

!ngrok authtoken 2KmLhi9o9rhTfgnwUY03qPNSw2p_3nUjkV6j5CBE73Xz2rWy3

!streamlit run --server.port 80 app.py &>/dev/null&

from pyngrok import ngrok 

public_url = ngrok.connect(port='80')

public_url






SQL


Command to create SQLlite connection to database:

conn = sqlite3.connect('pulse.db')

c = conn.cursor()

Example for creating tables:

c.execute('''CREATE TABLE IF NOT EXISTS Agg_State(
            State TEXT,
            Year TEXT,
            Quarter TEXT,
            Transacion_type TEXT,
            Transacion_count TEXT,
            Transacion_amount TEXT
            )''')
            
Inserting values to the table Example:

c.executemany('INSERT INTO Agg_State VALUES(?,?,?,?,?,?)', zip(stateaggr['State'], stateaggr['Year'], stateaggr['quarter'], stateaggr['Transacion_type'], stateaggr['Transacion_count'], stateaggr['Transacion_amount']))

Fetching data from a table :

x=c.execute("SELECT * FROM Agg_State")
x=c.fetchall()

