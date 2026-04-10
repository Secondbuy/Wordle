INPUT_FILE = "words.txt"
OUTPUT_FILE = "words_lua.txt"
WORDS_PER_LINE = 15

with open(INPUT_FILE, "r") as f:
    words = [line.strip().upper() for line in f if line.strip()]

chunks = [f'"{word}"' for word in words]
lines = []

for i in range(0, len(chunks), WORDS_PER_LINE):
    lines.append(",".join(chunks[i:i + WORDS_PER_LINE]))

lua_output = "local WORDS = {" + ",\n".join(lines) + "}"

with open(OUTPUT_FILE, "w") as f:
    f.write(lua_output)

print(f"Done! {len(words)} words written to {OUTPUT_FILE}")
