nom = ""  # Variable per guardar el nom de l'usuari
edat = 0  # Variable per guardar l'edat
pes = 0.0  # Variable per guardar el pes en kg
alcada = 0.0  # Variable per guardar l'alçada en metres
dades_introduides = False  # Boolean que indica si s'han introduït les dades

while True:
    # Mostrem el menú principal
    print("Menú principal")
    print("1. Introduir dades")
    print("2. Modificar dades")
    print("3. Visualitzar dades")
    print("4. Sortir")
    
    opcio = input("Selecciona una opció (1-4): ")  # Demanem a l'usuari que triï una opció

    match opcio:
        case "1":
            # Opció 1: introduir dades
            print("D'acord, anem a introduir les teves dades.")
            try:
                nom = input("Nom complet: ").capitalize()  # Sol·licitem el nom i posem la primera lletra en majúscula
                if nom == "":
                    print("Error: El nom no pot quedar buit.")
                    continue
                if nom.isnumeric:
                    print("El nom no pot ser un número")
                    continue
                if len(nom) < 2 or len(nom) > 742:
                    print("Error: El nom és incorrecte ")
                    continue
       
                edat = int(input("Edat: "))  # Demanem l'edat
                if edat <= 0 or edat > 120:
                    print("Error: L'edat ha de ser un enter positiu ≤ 120.")
                    continue

                pes = float(input("Pes (kg): ").replace(",", "."))  # Demanem el pes i permetem coma o punt
                if pes <= 0 or pes > 400:
                    print("Error: El pes ha de ser un número positiu raonable.")
                    continue

                alcada = float(input("Alçada (m): ").replace(",", "."))  # Demanem l'alçada
                if alcada <= 0.5 or alcada >= 2.5:
                    print("Error: L'alçada ha de ser entre 0.5 i 2.5 metres.")
                    continue

                # Guardem les dades
                dades_introduides = True
                print("Perfecte. Dades desades correctament.")

            except ValueError:
                print("Error: Format numèric invàlid. Torna-ho a provar.")

        case "2":
            # Opció 2: modificar dades
            if not dades_introduides:
                print("Encara no hi ha dades per modificar. Introdueix-les primer.")
                continue

            print("Quina dada vols modificar?")
            print("1. Nom complet")
            print("2. Edat")
            print("3. Pes")
            print("4. Alçada")
            eleccio = input("Tria 1-4: ")

            try:
                match eleccio:
                    case "1":
                        # Modificar nom
                        nou_nom = input("Escriu el nou nom complet: ").capitalize()
                        if nou_nom == "":
                            print("Error: El nom no pot quedar buit.")
                            continue
                        if nou_nom.isnumeric:
                            print("El nom no pot ser un número")
                            continue
                        if len(nou_nom) < 2 or len(nou_nom) > 742:
                            print("Error: El nom és incorrecte ")
                            continue
                        nom = nou_nom
                        print("Nom actualitzat correctament.")

                    case "2":
                        # Modificar edat
                        nova_edat = int(input("Escriu la nova edat: "))
                        if nova_edat <= 0 or nova_edat > 120:
                            print("Error: L'edat ha de ser un enter positiu ≤ 120.")
                            continue
                        edat = nova_edat
                        print("Edat actualitzada correctament.")

                    case "3":
                        # Modificar pes
                        nou_pes = float(input("Escriu el nou pes (kg): ").replace(",", "."))
                        if nou_pes <= 0 or nou_pes > 400:
                            print("Error: El pes ha de ser un número positiu raonable.")
                            continue
                        pes = nou_pes
                        print("Pes actualitzat correctament.")

                    case "4":
                        # Modificar alçada
                        nova_alcada = float(input("Escriu la nova alçada (m): ").replace(",", "."))
                        if nova_alcada <= 0.5 or nova_alcada >= 2.5:
                            print("Error: L'alçada ha de ser entre 0.5 i 2.5 metres.")
                            continue
                        alcada = nova_alcada
                        print("Alçada actualitzada correctament.")

                    case _:
                        print("No he entès l'opció que has posat.")
            except ValueError:
                print("Error: Format numèric invàlid. Torna-ho a provar.")

        case "3":
            # Opció 3: visualitzar dades
            if not dades_introduides:
                print("Encara no has introduït cap dada.")
            else:
                print("Això és el que tinc de tu fins ara:")
                print(f"Nom complet: {nom}")
                print(f"Edat: {edat} anys")
                print(f"Pes: {pes} kg")
                print(f"Alçada: {alcada} m")

                # Calculem 
                imc = pes / (alcada ** 2)
                print(f"El teu índex de massa corporal (IMC) és {imc:.2f}")
                if imc < 18.5:
                    print("Estàs per sota del pes recomanat.")
                elif 18.5 <= imc < 25:
                    print("Tens un pes saludable.")
                elif 25 <= imc < 30:
                    print("Estàs en sobrepès.")
                else:
                    print("Compte: obesitat.")

        case "4":
            # Opció 4: sortir del programa
            print("Sortint del programa")
            break

        case _:
            # Si no és cap opció vàlida
            print("Opció no vàlida. Tria entre 1 i 4.")