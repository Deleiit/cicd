debug:
	cargo build

release:
	RUSTFLAGS="-C codegen-units=1 -C code-model=kernel"
	cargo build --release --verbose
	strip target/release/simeis-server
	typst 

manuel:
	typst compile doc/manual.typ doc/manual.pdf

check:
	cargo check

test:
	cargo test

clean:
	cargo clean