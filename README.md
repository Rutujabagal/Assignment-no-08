H2SO4_req = float(input(“Enter the volume of H2SO4 required in ml: “))

# Input value of sample in liters

Sample = float(input(“Enter the value of sample in liters: “))

# Calculate alkalinity removed (mg/L)

Alkalinity_Removed = H2SO4_req

Print(“Alkalinity Removed: “, Alkalinity_Removed, “mg”)

# Calculate total alkalinity (mg/L)

Alk_mgperlit = Alkalinity_Removed / Sample

Print(“Total Alkalinity:”, Alk_mgperlit, “mg/l”)

# Input OH-Alkalinity present

OH = float(input(“Enter the value of OH-Alkalinity present: “))

# Calculate alkalinity removed till pH of 8.3

H2SO4_req_pH83 = float(input(“Enter the volume of H2SO4 required till pH 8.3 in ml: “))

Alkalinity_Removed_pH83 = H2SO4_req_pH83

Print(“Alkalinity Removed till pH 8.3:”, Alkalinity_Removed_pH83, “mg”)

# Calculate Carbonate Alkalinity

CO3_Combined = Alkalinity_Removed_pH83 / Sample

Print(“Carbonate Alkalinity upto pH 8.3:”, CO3_Combined, “mg/l”)

# Calculate actual Carbonate Alkalinity

CO3 = CO3_Combined – OH

Print(“Carbonate Alkalinity:”, CO3, “mg/l”)

# Calculate Bicarbonate Alkalinity

HCO3 = Alk_mgperlit – (2 * CO3) – OH

Print(“Bicarbonate Alkalinity:”, HCO3, “mg/l”)
