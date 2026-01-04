.PHONY: all clean

output/pdf/main-sch.pdf: main.kicad_sch
		kicad-cli sch export pdf --output "output/pdf/main-sch.pdf" main.kicad_sch

output/pdf/main-pcb.pdf: main.kicad_pcb
		kicad-cli pcb export pdf --output "output/pdf/main-pcb.pdf" -l B.Cu,Edge.Cuts,F.Cu main.kicad_pcb 

all: output/pdf/main-pcb.pdf output/pdf/main-sch.pdf

clean:
		rm -rf output/pdf/main-pcb.pdf output/pdf/main-sch.pdf
