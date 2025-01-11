# Μεταδεδομένα AI-NFT

Η δημιουργία AI-NFT είναι ακριβώς όπως τα παραδοσιακά NFT, **με** ένα επιπλέον πεδίο «ai_agent» που περιγράφει τη διαμόρφωση ενός πράκτορα AI και τη μηχανή που χρησιμοποιεί, αποθηκευμένα στα μεταδεδομένα.

## Υποστηριζόμενη μηχανή AI <a href="#metadata-json" id="metadata-json"></a>

<table><thead><tr><th width="224">Μηχανή</th><th width="231">Όνομα κινητήρα</th><th>Αρχείο χαρακτήρων</th></tr>< /thead><tbody><tr><td><a href="https://github.com/elizaOS/eliza">Eliza</a> από ElizaOS</td><td>eliza</td>< td><ul><li><a href="https://elizaos.github.io/eliza/docs/core/characterfile/">Τεκμηρίωση</a></li><li><a href="https://github.com/elizaOS/ characterfile">Πρότυπο</a></li><li><a href="https://github.com/elizaOS/eliza/tree/main/characters">Παράδειγμα</a></li></ul></td></tr></tbody></table >

## Μεταδεδομένα AI-NFT JSON <a href="#metadata-json" id="metadata-json"></a>

| Πεδίο | Τύπος | Περιγραφή |
| ----------------------------- | ------ | -------------------------------------------------- ------------------- -------------------------------------------------- ------------------- -------------------------------------------------- ------------------- -------------------------------------------------- ------------------- -------------------------------------------------- ------------------- -------------------------------------------------- ------------------- -------------------------------------------------- ------------------- -------------------------------------------------- -------------------- |
| **ai\_agent** (Προστέθηκε πρόσφατα) | αντικείμενο | <p>Η διαμόρφωση που καθορίζει τον πράκτορα AI που συνδέεται με αυτό το NFT. </p><ul><li><strong>μηχανή</strong> (string): ο κινητήρας που χρησιμοποιείται για τη λειτουργία του παράγοντα AI. Προεπιλογή ως "eliza".</li><li><strong>χαρακτήρας</strong> (αντικείμενο): το αρχείο χαρακτήρων JSON που περιγράφει έναν πράκτορα AI. Ελέγξτε <a href="https://github.com/elizaOS/characterfile?tab=readme-ov-file">εδώ</a>.</li></ul> |
| **όνομα** | χορδή | Όνομα του περιουσιακού στοιχείου. |
| **περιγραφή** | χορδή | Περιγραφή του περιουσιακού στοιχείου. |
| **εικόνα** | χορδή | URI που δείχνει το λογότυπο του στοιχείου. |
| **animation\_url** | χορδή | URI που δείχνει την κινούμενη εικόνα του στοιχείου. |
| **εξωτερική\_url** | χορδή | URI που δείχνει σε μια εξωτερική διεύθυνση URL που καθορίζει το στοιχείο — π.χ. τον κύριο ιστότοπο του παιχνιδιού. |
| **χαρακτηριστικά** | συστοιχία | <p>Πίνακας χαρακτηριστικών που καθορίζουν τα χαρακτηριστικά του στοιχείου.</p><ul><li><strong>trait_type</strong> (string): Ο τύπος του χαρακτηριστικού.</li><li><strong> value</strong> (string): Η τιμή για αυτό το χαρακτηριστικό.</li></ul> |
| **ιδιοκτησίες** | αντικείμενο | <p>Πρόσθετες ιδιότητες που καθορίζουν το στοιχείο.</p><ul><li><p><strong>αρχεία</strong> (πίνακας): Πρόσθετα αρχεία που πρέπει να συμπεριληφθούν με το στοιχείο.</p><ul> <li><strong>uri</strong> (string): Το URI του αρχείου.</li><li><strong>type</strong> (string): Ο τύπος του αρχείου. Π.χ. <code>image/png</code>, <code>video/mp4</code>, κ.λπ.</li><li><strong>cdn</strong> (boolean, προαιρετικό): Εάν το αρχείο εμφανίζεται από ένα CDN.</li></ul></li><li><strong>κατηγορία</strong> (string): Μια κατηγορία μέσων για το στοιχείο. Π.χ. <code>βίντεο</code>, <code>εικόνα</code> κ.λπ.</li></ul> |

## Παράδειγμα

```json
{
  // Πεδίο αντιπροσώπου AI
  ai_agent: {
    engine: "eliza",
    character: {
      // όνομα πράκτορα
      name:"eliza",
      // δηλώσεις φόντου
      bio: [
        "Οι βιογραμμές είναι κάθε σύντομο απόσπασμα που μπορεί να συντεθεί μαζί με τυχαία σειρά.",
        "Βρήκαμε ότι αυξάνει την εντροπία για να τυχαιοποιήσει και να επιλέξει μόνο μέρος του βιογραφικού για κάθε πλαίσιο.",
        "Αυτή η «εντροπία» χρησιμεύει για τη διεύρυνση της κατανομής των πιθανών εξόδων, οι οποίες θα πρέπει να δίνουν πιο ποικίλες αλλά συνεχώς σχετικές απαντήσεις."
      ],
      lore: [
        "Οι γραμμές lore είναι κάθε σύντομο απόσπασμα που μπορεί να συντεθεί μαζί με τυχαία σειρά, ακριβώς όπως το βιογραφικό",
        "Ωστόσο, αυτές είναι συνήθως πιο πραγματικές ή ιστορικές και λιγότερο βιογραφικές από βιογραφικές γραμμές",
        "Οι παραδόσεις μπορούν να εξαχθούν από chatlogs και tweets ως πράγματα που ο χαρακτήρας ή που του συνέβη",
        "Το Lore θα πρέπει επίσης να τυχαιοποιηθεί και να γίνει δειγματοληψία για να αυξηθεί η εντροπία στο πλαίσιο"
        ],
      ... //xxx.character.json from https://github.com/elizaOS/eliza/tree/main/characters
    }
  },
  // τυπικό πρότυπο μεταδεδομένων NFT
  name: 'Το NFT μου',
  description: 'Αυτό είναι ένα NFT στο Solana',
  image: imageUri[0],
  external_url: 'https://example.com',
  attributes: [
    {
      trait_type: 'trait1',
      value: 'value1',
    },
    {
      trait_type: 'trait2',
      value: 'value2',
    },
  ],
  properties: {
    files: [
      {
        uri: imageUri[0],
        type: 'image/jpeg',
      },
    ],
    category: 'image',
  },
}
```