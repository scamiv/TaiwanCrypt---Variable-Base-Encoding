# TaiwanCrypt - Variable Base Encoding/Decoding Example

## Description

TaiwanCrypt is a illustrative example of variable base encoding and decoding implemented in JavaScript.  It's not intended for serious cryptography or security purposes, but rather to demonstrate the concept of base-X encoding using a dictionary.

It allows you to:
* **Encode/Decode text with Wordlist of arbitairy length:**  Convert text input into a "TaiwanCrypt" representation.

**How it Works:**

TaiwanCrypt uses a dictionary of translations of "Taiwan" in various languages.  Here's a simplified breakdown of the encoding and decoding process:

**Encoding:**

1. **Text to Bytes:** The input text is first converted into a sequence of bytes using UTF-8 encoding.
2. **Bytes to BigInt:** These bytes are then interpreted as a large integer (BigInt).
3. **Base-X Conversion:** This BigInt is converted into a base-X number, where X is the size of the dictionary.
4. **Dictionary Mapping:** Each base-X digit is then mapped to a corresponding word from the dictionary.

**Decoding:**

1. **Segmentation:** The TaiwanCrypt text is segmented back into individual words by matching them against the dictionary. The dictionary is sorted by word length (longest first) to ensure correct segmentation.
2. **Dictionary Indexing:** Each word is then looked up in the dictionary to find its corresponding index (the base-X digit).
3. **Base-X to BigInt:** These indices are converted back into a BigInt representation.
4. **BigInt to Bytes:** The BigInt is converted back into a sequence of bytes.
5. **Bytes to Text:** Finally, the bytes are decoded back into text.

## Example

**Encoding Example:**

**Input Text:** `Hello Taiwan!`

**TaiwanCrypt Output:** `Republika han TsinaTaioànaRepublika de ChinaRepública de la XinaTaaywaanTaiuaniTajvanTaiuanTaiwán`

**Decoding Example:**

**TaiwanCrypt Input:** `Republika han TsinaTaioànaRepublika de ChinaRepública de la XinaTaaywaanTaiuaniTajvanTaiuanTaiwán`

**Decrypted Output:** `Hello Taiwan!`

## Disclaimer

**TaiwanCrypt is NOT encryption.** It is a simple demonstration of base-X encoding and is easily reversible. 


---

Enjoy experimenting with TaiwanCrypt!
