# AP Computer Science Principles Unit 2: Data

> How computers represent, store, and process information using bits. This unit covers binary numbers, abstraction, data compression, analog vs digital, metadata, and big data.

**Practice all Unit 2 questions, flashcards, and Create Task prep →** [apscore5.com/ap-computer-science-principles/unit-2-data](https://www.apscore5.com/ap-computer-science-principles/unit-2-data)

---

## What is Unit 2 about?

Unit 2 of AP Computer Science Principles studies how computers handle data. Everything inside a computer — text, images, sounds, video — is ultimately stored as **bits** (0s and 1s). You'll learn how binary works, how different data types are represented, how data compression saves space, the difference between analog and digital, and how big data is collected, analyzed, and used. This unit makes up about 17–22% of the exam — one of the highest-weight units — and shows up frequently in questions about binary conversion, data representation, and data analysis.

---

## Microtopics in this unit

*Microtopic pages are being added. Check back soon, or visit the [full Unit 2 course on apscore5.com](https://www.apscore5.com/ap-computer-science-principles/unit-2-data) for complete content.*

---

## Key concepts to master

### Bits and bytes

Computers store and process all data using **bits** — the smallest unit of information.

| Unit | Size |
|---|---|
| **Bit** | A single 0 or 1 |
| **Byte** | 8 bits |
| **Kilobyte (KB)** | ~1,000 bytes |
| **Megabyte (MB)** | ~1 million bytes |
| **Gigabyte (GB)** | ~1 billion bytes |
| **Terabyte (TB)** | ~1 trillion bytes |

**Why binary?** Computer hardware uses electrical signals — easy to represent two states (on/off, high/low voltage) using just 0 and 1.

---

## Binary numbers

Binary is a **base-2** number system. Each position represents a power of 2.

### Binary place values

| Bit position | Value (power of 2) | Decimal value |
|---|---|---|
| Position 0 (rightmost) | 2⁰ | 1 |
| Position 1 | 2¹ | 2 |
| Position 2 | 2² | 4 |
| Position 3 | 2³ | 8 |
| Position 4 | 2⁴ | 16 |
| Position 5 | 2⁵ | 32 |
| Position 6 | 2⁶ | 64 |
| Position 7 | 2⁷ | 128 |

### Binary to decimal conversion

Add up the place values where there's a 1.

**Example:** Convert `10110` to decimal:
- 1 × 16 = 16
- 0 × 8 = 0
- 1 × 4 = 4
- 1 × 2 = 2
- 0 × 1 = 0
- **Total = 22**

### Decimal to binary conversion

Find the largest power of 2 that fits, subtract, and repeat.

**Example:** Convert 13 to binary:
- 13 = 8 + 4 + 1
- 8 (2³) = 1, 4 (2²) = 1, 2 (2¹) = 0, 1 (2⁰) = 1
- **Result: 1101**

### How many values can N bits represent?

**Formula: 2ⁿ values**

| Bits | Values | Examples |
|---|---|---|
| **1 bit** | 2 (0 or 1) | On/off |
| **2 bits** | 4 (00, 01, 10, 11) | 4 colors |
| **3 bits** | 8 | 8 directions |
| **4 bits** | 16 | 16 colors |
| **8 bits (1 byte)** | 256 | One character (ASCII) |
| **16 bits** | 65,536 | Unicode characters |
| **24 bits** | 16,777,216 | RGB color values |
| **32 bits** | ~4.3 billion | Standard integer range |

---

## Abstraction

**Abstraction** = hiding complexity by showing only what's needed.

### Levels of abstraction in computing

| Level | What it represents |
|---|---|
| **Hardware** | Transistors and circuits |
| **Binary** | 0s and 1s |
| **Machine code** | Instructions the CPU understands |
| **Assembly language** | Human-readable shortcuts for machine code |
| **High-level languages** | Python, Java, JavaScript |
| **User interface** | What the user sees and interacts with |

**Example:** When you click "save" in a document, you don't need to know how the file system writes bits to a disk. The "save" button is an abstraction over a complex process.

### Abstraction in programming

| Type | What it does |
|---|---|
| **Procedures (functions)** | Hide the details of a process behind a name |
| **Variables** | Hide actual memory locations behind a label |
| **Data types** | Hide bit-level representation behind a category (integer, string) |
| **APIs** | Hide complex services behind simple commands |

---

## Representing different types of data

### Text (characters)

Each character is mapped to a number, which is stored in binary.

| Standard | What it covers |
|---|---|
| **ASCII** | 128 characters (English letters, digits, basic symbols) — 7 bits |
| **Extended ASCII** | 256 characters (adds Western European symbols) — 8 bits |
| **Unicode (UTF-8/16)** | 1+ million characters — supports all languages, emojis, symbols |

### Images

Images are stored as **pixels** — each pixel has a color value.

| Color model | What it stores |
|---|---|
| **RGB** | Red, Green, Blue — typically 8 bits each (256 levels) — total 24 bits per pixel |
| **Grayscale** | Single brightness value (8 bits = 256 shades of gray) |
| **Black and white** | 1 bit per pixel (0 or 1) |

**Image size = width × height × bits per pixel**

### Sound

Sound is **analog** (continuous wave). Computers must convert it to **digital** (discrete samples).

| Concept | What it means |
|---|---|
| **Sample rate** | How often the sound wave is measured per second (Hz) |
| **Bit depth** | How many bits represent each sample |
| **Higher sample rate + bit depth** | Better quality, larger file |

**CD-quality audio:** 44,100 samples per second × 16 bits per sample × 2 channels (stereo).

### Video

Video = many images (frames) shown rapidly + audio.

- Typical video: 24–60 frames per second
- Each frame is a full image
- Video files are huge → almost always compressed

---

## Analog vs digital data

| Type | What it is | Examples |
|---|---|---|
| **Analog** | Continuous values (any value in a range) | Sound waves, light, temperature, vinyl records |
| **Digital** | Discrete values (specific values only) | All computer data, CDs, MP3s, JPEGs |

**Conversion:** real-world (analog) → samples (digital).

**Loss in conversion:** taking discrete samples of a continuous wave **always** loses some detail. Higher sampling rates and bit depths reduce loss but never eliminate it.

---

## Data compression

Reducing the size of data so it takes less space and transmits faster.

### Two types of compression

| Type | What happens | When to use |
|---|---|---|
| **Lossless** | Original data is **fully recoverable** after decompression | Text, code, medical images, anything where exactness matters |
| **Lossy** | Some data is **permanently discarded** to save more space | Photos, music, video, where small quality loss is acceptable |

### Examples

| Format | Type |
|---|---|
| **ZIP, PNG, FLAC, GIF** | Lossless |
| **JPEG, MP3, MP4, AAC** | Lossy |

### Trade-offs

- Lossless = better quality, larger files
- Lossy = smaller files, lower quality (often unnoticeable)
- Choose based on the use case

---

## Metadata

**Data about data.** Metadata describes the data without being part of the data itself.

### Examples of metadata

| Data | Metadata |
|---|---|
| **Photo** | Date taken, camera model, GPS location, file size, resolution |
| **Music file** | Title, artist, album, length, bitrate |
| **Document** | Author, last modified date, file format, word count |
| **Email** | Sender, recipient, timestamp, subject |
| **Webpage** | Page title, description, keywords, author |

### Why metadata matters

- **Search and organization** — find photos taken in a specific city, sort music by artist
- **Authentication** — verify when a document was created
- **Privacy concerns** — metadata can reveal a lot (location, habits, social network)
- **Forensics** — investigators use metadata in legal cases

---

## Data and information

| Term | What it means |
|---|---|
| **Data** | Raw facts and numbers, often without context |
| **Information** | Data that's been processed, organized, or interpreted to be useful |
| **Knowledge** | Information combined with experience and context |
| **Insight** | Knowledge that drives decisions |

**Example:**
- **Data:** 78, 65, 92, 88, 71
- **Information:** "Test scores in Mr. Smith's class"
- **Knowledge:** "The average score is 78.8, similar to last year's class"
- **Insight:** "We should review topic X — most students missed those questions"

---

## Big data

Massive datasets that can't be processed with traditional methods.

### Characteristics (the "Vs")

| V | What it means |
|---|---|
| **Volume** | Huge amounts of data (terabytes, petabytes) |
| **Velocity** | Generated very fast |
| **Variety** | Many types and sources (text, images, video, sensor data) |
| **Veracity** | Quality and reliability of data |

### Sources of big data

- Social media (every post, like, comment)
- Mobile phones (location, app usage)
- Online transactions (purchases, browsing)
- Sensors (IoT, weather, traffic)
- Government records, healthcare, finance

### Uses of big data

- **Targeted advertising** (showing ads based on your behavior)
- **Recommendation engines** (Netflix, Spotify, YouTube)
- **Disease tracking** (COVID-19 spread)
- **Smart cities** (traffic, energy, air quality)
- **Scientific research** (genomics, astronomy)

### Concerns with big data

- **Privacy** — your data is collected, sold, analyzed without your full awareness
- **Bias** — algorithms can amplify existing societal biases
- **Security** — large datasets are targets for hackers
- **Surveillance** — governments and corporations track behavior

---

## Cleaning and analyzing data

### Cleaning data

Real-world data is messy. Before analysis, data often needs to be cleaned:

| Issue | Fix |
|---|---|
| **Missing values** | Fill in, estimate, or remove the row |
| **Duplicate entries** | Remove duplicates |
| **Inconsistent formatting** | Standardize (dates, names, capitalization) |
| **Errors and typos** | Fix or flag |
| **Outliers** | Decide whether to keep or remove |

### Tools for analysis

| Tool | What it does |
|---|---|
| **Spreadsheets (Excel, Google Sheets)** | Sort, filter, basic calculations, charts |
| **Databases** | Store and query large structured datasets (SQL) |
| **Programming languages** | Custom analysis (Python, R) |
| **Visualization tools** | Tableau, charts in spreadsheets |

### Visualizing data

| Chart | When to use |
|---|---|
| **Bar chart** | Compare categories |
| **Line chart** | Show change over time |
| **Pie chart** | Show parts of a whole |
| **Scatter plot** | Show relationships between two variables |
| **Histogram** | Show distribution of values |
| **Heatmap** | Show patterns in 2D data |

---

## Common AP exam mistakes

- **Forgetting that AP CSP doesn't always start counting at 0** — but binary place values do start at 2⁰
- **Confusing analog and digital** — analog is continuous; digital is discrete
- **Mixing up lossless and lossy compression** — lossless preserves original; lossy discards data
- **Calculating bits incorrectly** — N bits = 2ⁿ values, not n × 2
- **Forgetting about metadata in privacy questions** — even without "real" data, metadata reveals a lot
- **Confusing data with information** — raw numbers (data) become useful only after processing (information)
- **Saying "more bits = always better"** — there's a trade-off with file size and processing time
- **Thinking compression is always lossless** — JPEG and MP3 lose data permanently

---

## How Unit 2 connects to other units

- **Unit 1 (Creative Development)** — programs work with data; data types affect program behavior
- **Unit 3 (Algorithms and Programming)** — algorithms operate on data; lists store data
- **Unit 4 (Computer Systems)** — networks transmit data; protocols define data formats
- **Unit 5 (Impact of Computing)** — privacy, bias, and security all relate to data collection and use

---

## Top exam topics to prepare

1. **Binary conversion** — convert between binary and decimal
2. **Bit calculations** — given N bits, calculate the number of possible values (2ⁿ)
3. **Abstraction** — explain how abstraction simplifies complexity
4. **Lossless vs lossy compression** — choose the right type for a scenario
5. **Analog vs digital** — explain conversion and quality trade-offs
6. **Metadata and privacy** — explain how metadata can reveal personal information
7. **Big data uses and concerns** — describe both sides
8. **Reading data visualizations** — interpret bar charts, line graphs, scatter plots

---

## Frequently asked

**How much of the AP exam is Unit 2?**
Unit 2 makes up about 17–22% of multiple-choice questions. Binary conversion, data representation, and compression are the most-tested concepts. Roughly 1 in 5 exam questions comes from this unit.

**Why does everything need to be in binary?**
Computer hardware works with electrical signals that are either on or off (high or low voltage). Two states are easy and reliable to detect — three or more would be more error-prone. Binary (0s and 1s) maps perfectly onto these two states. All other data — text, images, sounds — must ultimately be represented in this 2-state system.

**What's the difference between lossless and lossy compression?**
Lossless compression reduces file size without losing any data — when decompressed, the file is exactly the same as the original. Examples: ZIP, PNG, FLAC. Lossy compression discards some data permanently to achieve much smaller files. Examples: JPEG (photos), MP3 (music), MP4 (video). Lossy is fine for media where small quality loss is unnoticeable, but bad for text or code where every bit matters.

**How does N bits give 2ⁿ possible values?**
Each bit can be 0 or 1 — that's 2 options. With 2 bits, each can independently be 0 or 1, so the total combinations are 2 × 2 = 4 (00, 01, 10, 11). With 3 bits, it's 2 × 2 × 2 = 8. The pattern is 2ⁿ. So 8 bits = 2⁸ = 256 possible values.

**What is metadata and why is it a privacy concern?**
Metadata is data about data — for a photo, it's information like when it was taken, what camera, where (GPS), and the device used. Even if you don't share the photo's content, the metadata reveals a lot — your location, your habits, the equipment you own. Email metadata reveals who you communicate with, when, and how often, even without reading the messages themselves. This is why privacy advocates worry as much about metadata collection as the actual content.

**What's the difference between analog and digital?**
Analog data is continuous — it can take any value within a range, like a smooth sound wave or a vinyl record's grooves. Digital data is discrete — it can only take specific values, sampled from the analog source. When you convert analog to digital (recording sound, scanning a photo), you take samples at intervals. Higher sampling rates capture more detail but produce larger files.

**Why is big data a big deal?**
Big data refers to datasets too large for traditional tools to handle. It's a big deal because it enables things that weren't possible before — disease tracking, personalized recommendations, real-time traffic analysis, scientific breakthroughs in genomics. But it also raises serious concerns about privacy (your data is constantly collected), bias (algorithms can amplify discrimination), and surveillance (corporations and governments track behavior at scale).

**Are JPEGs really lossy?**
Yes. JPEG compression discards data your eye is unlikely to notice (subtle color variations, fine details). Once compressed, you can't recover the original — saving a JPEG repeatedly causes more loss each time. For photos, this is usually fine. But for images that need to stay perfect (medical imaging, technical diagrams, art), use a lossless format like PNG.

---

## Practice this unit

- [Full Unit 2 guide on apscore5.com](https://www.apscore5.com/ap-computer-science-principles/unit-2-data) — 50+ questions, flashcards, Create Task prep
- [Browse all AP CSP units](../)
- [AP CSP course overview](../../ap-computer-science-principles/)

---

*Notes synced from [apscore5.com](https://www.apscore5.com/ap-computer-science-principles/unit-2-data). Last updated: May 2026.*
