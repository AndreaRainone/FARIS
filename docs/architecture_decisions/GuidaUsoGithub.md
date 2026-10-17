# **WORKFLOW Git & GitHub** - Linee guida all'organizzazione della repository.

Definizione del flusso di lavoro obbligatorio per tutti i membri del team.

*REGOLA: nessuno pusha direttamente sul branch 'main'. Lì finisce solo il codice già revisionato e approvato tramite Pull Request.*
----------------------------------------------------------------------------------------------------

# FLUSSO DI LAVORO:
## ***1. Sync dello spazio di lavoro***
**Prima di editare il codice, assicurarsi di avere l'ultima versione disponibile:**

    ```bash

    git checkout main
    git pull origin main

## ***2. Creazione Branch di Lavoro***
**Per ogni Task e/o Sub-Task assegnato (a meno di blocchi contigui e correlati), lavorare su un branch dedicato.**

    ```bash

    git switch -c nomeBranch


## ***3. Review e Pull Request***
**Prima di fare il push di qualche modifica effettuare questi passaggi:**

1. Muoversi nella cartella dove si desidera effettuare il push e poi:

    ```bash

    git add .
    //oppure
    git add nomeFile.nomeEstensione

    git commit -m "CODICE_TASKJIRA Commento"
    //esempio: 
    "git commit -m "ISFARIS-3 Aggiunto obiettivi del sistema"
    
    git push -u origin nomeBranch

2. Entrare poi sulla repository di github, aprire una pull request e assegnare un "Reviewer" (Andrea / Davide) diverso dall'autore.
3. Entrare sullo spazio di progetto di Jira e cambiare lo stato dei task/sottotask in "Revisione".
4. Scrivere nella sezione "Comunicazioni" di Discord, taggando il revisore e avvertendolo di revisionare quel task

## ***4. Altri comandi utili per gestire i branch***

    ```bash

    #Muoversi tra i branch

    git switch nomeBranch
    
    git restore . //per ripristinare tutti i file modificati nella cartella corrente
    git restore nomeFile.estensione //per annullare le modifiche al file e riportarlo all'ultimo commit

----------------------------------------------------------------------------------------------------

***Nota a margine***: 
dopo essere stato revisionato il push sarà fatto da chi lo ha revisionato, ma risulterà comunque richiesto dal membro del team originale, quindi la traccia del lavoro svolto rimarrà.

    
