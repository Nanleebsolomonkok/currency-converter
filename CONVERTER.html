import tkinter as tk
from tkinter import ttk, messagebox
import requests
import json
import threading
from datetime import datetime

API_URL = "https://open.er-api.com/v6/latest/USD"

# Some currency full names for display (partial)
CURRENCY_NAMES = {
  "AED": "United Arab Emirates Dirham",
  "AFN": "Afghan Afghani",
  "ALL": "Albanian Lek",
  "AMD": "Armenian Dram",
  "ANG": "Netherlands Antillean Guilder",
  "AOA": "Angolan Kwanza",
  "ARS": "Argentine Peso",
  "AUD": "Australian Dollar",
  "AWG": "Aruban Florin",
  "AZN": "Azerbaijani Manat",

  "BAM": "Bosnia-Herzegovina Convertible Mark",
  "BBD": "Barbadian Dollar",
  "BDT": "Bangladeshi Taka",
  "BGN": "Bulgarian Lev",
  "BHD": "Bahraini Dinar",
  "BIF": "Burundian Franc",
  "BMD": "Bermudian Dollar",
  "BND": "Brunei Dollar",
  "BOB": "Bolivian Boliviano",
  "BRL": "Brazilian Real",
  "BSD": "Bahamian Dollar",
  "BTN": "Bhutanese Ngultrum",
  "BWP": "Botswana Pula",
  "BYN": "Belarusian Ruble",
  "BZD": "Belize Dollar",

  "CAD": "Canadian Dollar",
  "CDF": "Congolese Franc",
  "CHF": "Swiss Franc",
  "CLP": "Chilean Peso",
  "CNY": "Chinese Yuan",
  "COP": "Colombian Peso",
  "CRC": "Costa Rican Colón",
  "CUP": "Cuban Peso",
  "CVE": "Cape Verdean Escudo",
  "CZK": "Czech Koruna",

  "DJF": "Djiboutian Franc",
  "DKK": "Danish Krone",
  "DOP": "Dominican Peso",
  "DZD": "Algerian Dinar",

  "EGP": "Egyptian Pound",
  "ERN": "Eritrean Nakfa",
  "ETB": "Ethiopian Birr",
  "EUR": "Euro",

  "FJD": "Fijian Dollar",
  "FKP": "Falkland Islands Pound",

  "GBP": "British Pound Sterling",
  "GEL": "Georgian Lari",
  "GHS": "Ghanaian Cedi",
  "GIP": "Gibraltar Pound",
  "GMD": "Gambian Dalasi",
  "GNF": "Guinean Franc",
  "GTQ": "Guatemalan Quetzal",
  "GYD": "Guyanese Dollar",

  "HKD": "Hong Kong Dollar",
  "HNL": "Honduran Lempira",
  "HRK": "Croatian Kuna",
  "HTG": "Haitian Gourde",
  "HUF": "Hungarian Forint",

  "IDR": "Indonesian Rupiah",
  "ILS": "Israeli New Shekel",
  "INR": "Indian Rupee",
  "IQD": "Iraqi Dinar",
  "IRR": "Iranian Rial",
  "ISK": "Icelandic Króna",

  "JMD": "Jamaican Dollar",
  "JOD": "Jordanian Dinar",
  "JPY": "Japanese Yen",

  "KES": "Kenyan Shilling",
  "KGS": "Kyrgyzstani Som",
  "KHR": "Cambodian Riel",
  "KMF": "Comorian Franc",
  "KRW": "South Korean Won",
  "KWD": "Kuwaiti Dinar",
  "KYD": "Cayman Islands Dollar",
  "KZT": "Kazakhstani Tenge",

  "LAK": "Lao Kip",
  "LBP": "Lebanese Pound",
  "LKR": "Sri Lankan Rupee",
  "LRD": "Liberian Dollar",
  "LSL": "Lesotho Loti",
  "LYD": "Libyan Dinar",

  "MAD": "Moroccan Dirham",
  "MDL": "Moldovan Leu",
  "MGA": "Malagasy Ariary",
  "MKD": "Macedonian Denar",
  "MMK": "Myanmar Kyat",
  "MNT": "Mongolian Tögrög",
  "MOP": "Macanese Pataca",
  "MRU": "Mauritanian Ouguiya",
  "MUR": "Mauritian Rupee",
  "MVR": "Maldivian Rufiyaa",
  "MWK": "Malawian Kwacha",
  "MXN": "Mexican Peso",
  "MYR": "Malaysian Ringgit",
  "MZN": "Mozambican Metical",

  "NAD": "Namibian Dollar",
  "NGN": "Nigerian Naira",
  "NIO": "Nicaraguan Córdoba",
  "NOK": "Norwegian Krone",
  "NPR": "Nepalese Rupee",
  "NZD": "New Zealand Dollar",

  "OMR": "Omani Rial",

  "PAB": "Panamanian Balboa",
  "PEN": "Peruvian Sol",
  "PGK": "Papua New Guinean Kina",
  "PHP": "Philippine Peso",
  "PKR": "Pakistani Rupee",
  "PLN": "Polish Złoty",
  "PYG": "Paraguayan Guaraní",

  "QAR": "Qatari Riyal",

  "RON": "Romanian Leu",
  "RSD": "Serbian Dinar",
  "RUB": "Russian Ruble",
  "RWF": "Rwandan Franc",

  "SAR": "Saudi Riyal",
  "SBD": "Solomon Islands Dollar",
  "SCR": "Seychellois Rupee",
  "SDG": "Sudanese Pound",
  "SEK": "Swedish Krona",
  "SGD": "Singapore Dollar",
  "SLL": "Sierra Leonean Leone",
  "SOS": "Somali Shilling",
  "SRD": "Surinamese Dollar",
  "SSP": "South Sudanese Pound",
  "STN": "São Tomé and Príncipe Dobra",
  "SYP": "Syrian Pound",
  "SZL": "Eswatini Lilangeni",

  "THB": "Thai Baht",
  "TJS": "Tajikistani Somoni",
  "TMT": "Turkmenistani Manat",
  "TND": "Tunisian Dinar",
  "TOP": "Tongan Paʻanga",
  "TRY": "Turkish Lira",
  "TTD": "Trinidad and Tobago Dollar",
  "TZS": "Tanzanian Shilling",

  "UAH": "Ukrainian Hryvnia",
  "UGX": "Ugandan Shilling",
  "USD": "United States Dollar",
  "UYU": "Uruguayan Peso",
  "UZS": "Uzbekistani Som",

  "VES": "Venezuelan Bolívar",
  "VND": "Vietnamese Đồng",

  "WST": "Samoan Tala",

  "XAF": "Central African CFA Franc",
  "XCD": "East Caribbean Dollar",
  "XOF": "West African CFA Franc",
  "XPF": "CFP Franc",

  "YER": "Yemeni Rial",

  "ZAR": "South African Rand",
  "ZMW": "Zambian Kwacha",
  "ZWL": "Zimbabwean Dollar"
}


class CurrencyConverterApp(tk.Tk):
    def __init__(self):
        super().__init__()
        self.title("Advanced Currency Converter")
        self.geometry("450x450")
        self.resizable(True, False)
        self.configure(bg="#0B132B")

        self.rates = {}
        self.last_update_unix = 0
        self.currencies = []

        # Variables
        self.from_currency_var = tk.StringVar()
        self.to_currency_var = tk.StringVar()
        self.amount_var = tk.StringVar()
        self.result_var = tk.StringVar()
        self.status_var = tk.StringVar()

        self.create_widgets()
        self.fetch_rates_async()

    def create_widgets(self):
        # StylingZX
        style = ttk.Style(self)
        style.theme_use('clam')
        style.configure("TLabel", background="#764ba2", foreground="white", font=("Poppins", 11))
        style.configure("TButton",
                        font=("Poppins", 11, "bold"),
                        foreground="white",
                        background="#6c63ff",
                        padding=6)
        style.configure("TEntry",
                        font=("Poppins", 11))
        style.configure("TCombobox",
                        font=("Poppins", 11),
                        foreground="#343")

        # Title
        title = ttk.Label(self, text="Currency Converter", font=("Poppins", 18, "bold"))
        title.pack(pady=(15, 10))

        frame = ttk.Frame(self)
        frame.pack(padx=20, pady=10, fill='x')

        # Amount Entry
        ttk.Label(frame, text="Amount:").grid(row=0, column=0, sticky='w', pady=5)
        amount_entry = ttk.Entry(frame, textvariable=self.amount_var)
        amount_entry.grid(row=0, column=1, sticky='ew', pady=5)
        amount_entry.focus()

        # From currency combobox
        ttk.Label(frame, text="From:").grid(row=1, column=0, sticky='w', pady=5)
        self.from_combo = ttk.Combobox(frame, textvariable=self.from_currency_var, state='readonly')
        self.from_combo.grid(row=1, column=1, sticky='ew', pady=5)

        # To currency combobox
        ttk.Label(frame, text="To:").grid(row=2, column=0, sticky='w', pady=5)
        self.to_combo = ttk.Combobox(frame, textvariable=self.to_currency_var, state='readonly')
        self.to_combo.grid(row=2, column=1, sticky='ew', pady=5)

        # Swap button
        self.swap_button = ttk.Button(frame, text="Swap ↔", command=self.swap_currencies)
        self.swap_button.grid(row=1, column=2, padx=10, sticky='ew', pady=5)

        # Convert button
        self.convert_button = ttk.Button(self, text="Convert", command=self.convert_currency)
        self.convert_button.pack(pady=12, ipadx=10)

        # Result label
        self.result_label = ttk.Label(self, textvariable=self.result_var, font=("Poppins", 14, "bold"), foreground="#ffd700")
        self.result_label.pack(pady=6)

        # Status label
        self.status_label = ttk.Label(self, textvariable=self.status_var, font=("Poppins", 9))
        self.status_label.pack(pady=3)

        # Configure grid weights
        frame.columnconfigure(1, weight=1)

    def fetch_rates_async(self):
        self.status_var.set("Loading exchange rates, please wait...")
        self.convert_button.config(state='disabled')
        self.swap_button.config(state='disabled')
        threading.Thread(target=self.fetch_rates).start()

    def fetch_rates(self):
        try:
            response = requests.get(API_URL, timeout=10)
            response.raise_for_status()
            data = response.json()
            if data.get("result") == "error":
                self.status_var.set("API error: " + data.get("error-type", "Unknown error"))
                self.convert_button.config(state='normal')
                self.swap_button.config(state='normal')
                return
            self.rates = data.get("rates", {})
            self.last_update_unix = data.get("time_last_update_unix", 0)
            self.currencies = sorted(self.rates.keys())
            self.update_currency_widgets()
            self.status_var.set("Exchange rates updated at " + self.format_timestamp(self.last_update_unix))
            self.convert_button.config(state='normal')
            self.swap_button.config(state='normal')
        except requests.Timeout:
            self.status_var.set("Connection timed out. Please check your internet connection.")
        except requests.ConnectionError:
            self.status_var.set("Network connection error. Please check your internet connection.")
        except requests.RequestException as e:
            self.status_var.set(f"Failed to load exchange rates: {str(e)}")
        except json.JSONDecodeError:
            self.status_var.set("Invalid response from the server.")
        except Exception as e:
            self.status_var.set(f"Unexpected error: {str(e)}")
        finally:
            self.convert_button.config(state='normal')
            self.swap_button.config(state='normal')

    def update_currency_widgets(self):
        # Add currency names if available for display as "CODE - Name"
        display_values = [f"{code} - {CURRENCY_NAMES.get(code, 'Unknown')}" for code in self.currencies]

        self.from_combo['values'] = display_values
        self.to_combo['values'] = display_values

        # Set defaults
        try:
            default_from_index = self.currencies.index("USD")
        except ValueError:
            default_from_index = 0
        try:
            default_to_index = self.currencies.index("GHS")
        except ValueError:
            default_to_index = 1 if len(self.currencies) > 1 else 0

        self.from_combo.current(default_from_index)
        self.to_combo.current(default_to_index)

    def swap_currencies(self):
        from_idx = self.from_combo.current()
        to_idx = self.to_combo.current()
        self.from_combo.current(to_idx)
        self.to_combo.current(from_idx)
        self.result_var.set("")
        self.status_var.set("")

    def convert_currency(self):
        try:
            amount_text = self.amount_var.get().strip()
            if not amount_text:
                messagebox.showwarning("Input Error", "Please enter the amount to convert.")
                return
            amount = float(amount_text)
            if amount < 0:
                messagebox.showwarning("Input Error", "Please enter a non-negative amount.")
                return
        except ValueError:
            messagebox.showwarning("Input Error", "Invalid amount entered. Please enter a numeric value.")
            return

        from_idx = self.from_combo.current()
        to_idx = self.to_combo.current()
        if from_idx == -1 or to_idx == -1:
            messagebox.showwarning("Selection Error", "Please select both currencies.")
            return

        from_code = self.currencies[from_idx]
        to_code = self.currencies[to_idx]

        if from_code == to_code:
            self.result_var.set(f"{amount:.2f} {from_code} = {amount:.2f} {to_code}")
            return

        try:
            usd_amount = amount / self.rates[from_code]
            converted_amount = usd_amount * self.rates[to_code]
            self.result_var.set(f"{amount:.2f} {from_code} = {converted_amount:.2f} {to_code}")
            self.status_var.set("")
        except Exception as e:
            messagebox.showerror("Conversion Error", f"Error during conversion: {str(e)}")
            self.result_var.set("")
            self.status_var.set("")

    @staticmethod
    def format_timestamp(unix_timestamp):
        if unix_timestamp == 0:
            return "Unknown time"
        dt = datetime.utcfromtimestamp(unix_timestamp)
        return dt.strftime("%Y-%m-%d %H:%M UTC")

if __name__ == "__main__":
    app = CurrencyConverterApp()
    app.mainloop()
