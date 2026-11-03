# Permet de compiler le code afin de créer des fichiers compilés/exécutables 
debug:
	cargo build

# Permet de compiler le code en précisant des variables optimisant les fichiers compilés/exécutables
release:
	RUSTFLAGS="-C codegen-units=1 -C code-model=kernel" cargo build --release --verbose
	strip target/release/simeis-server

# Permet de créer la doc en .pdf depuis un fichier .typ
manuel:
	typst compile doc/manual.typ doc/manual.pdf

# Permet de vérifier la qualité du code pré-compilation
check:
	cargo check

# Permet de vérifier que de mauvais schémas ne sont pas détectés
clippy:
	cargo clippy

# Permet de formater le code
fmt:
	cargo fmt --check

# Permet de tester le code unitairement
test:
	cargo test

anothertest:
	cargo test --features heavy-testing

anotherbuild:
	cargo build --features heavy-testing

# Permet de supprimer tous les fichiers compilés/exécutables lors de 'make release' ou 'make build'
clean:
	cargo clean

audit:
	cargo audit

udeps:
	cargo +nightly udeps