# Security Policyimport random
import string

def generer_code(longueur=12):
    caracteres = string.ascii_letters + string.digits
    return ''.join(random.choice(caracteres) for _ in range(longueur))

def generer_plusieurs_codes(nombre=10, longueur=12):
    codes = []
    for _ in range(nombre):
        codes.append(generer_code(longueur))
    return codes

if __name__ == "__main__":
    nombre = int(input("Combien de codes générer ? "))
    longueur = int(input("Longueur de chaque code ? "))

    resultats = generer_plusieurs_codes(nombre, longueur)

    print("\nCodes générés :\n")
    for code in resultats:
        print(code)

## Supported Versions

Use this section to tell people about which versions of your project are
currently being supported with security updates.

| Version | Supported          |
| ------- | ------------------ |
| 5.1.x   | :white_check_mark: |
| 5.0.x   | :x:                |
| 4.0.x   | :white_check_mark: |
| < 4.0   | :x:                |

## Reporting a Vulnerability

Use this section to tell people how to report a vulnerability.

Tell them where to go, how often they can expect to get an update on a
reported vulnerability, what to expect if the vulnerability is accepted or
declined, etc.
