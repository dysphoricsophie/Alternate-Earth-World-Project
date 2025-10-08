<%*
function generateName() {
    const prefixes = ["Ar", "Bel", "Cor", "Dra", "Fen", "Gor", "Kel", "Mor", "Tar", "Vor"];
    const middles = ["an", "or", "el", "is", "ur", "en", "al", "ir", "ul", "eth"];
    const suffixes = ["ath", "ion", "ar", "os", "iel", "um", "is", "or", "as", "an"];

    let prefix = prefixes[Math.floor(Math.random() * prefixes.length)];
    let middle = middles[Math.floor(Math.random() * middles.length)];
    let suffix = suffixes[Math.floor(Math.random() * suffixes.length)];

    return prefix + middle + suffix;
}

// Generate 10 names
let results = [];
for (let i = 0; i < 10; i++) {
    results.push(generateName());
}

// Insert into note
tR += "### Generated Names\n" + results.join(", ");
%>
