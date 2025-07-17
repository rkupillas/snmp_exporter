# Makefile for Cisco device family

# Define variables for clarity
GENERATOR := ./generator
GENERATOR_YML := generator.yml
OUTPUT_SNMP_YML := snmp.yml
LOCAL_MIBS := mibs/
COMMON_MIBS := ../common_mibs/

.PHONY: all clean generate

all: generate

generate: $(GENERATOR) $(GENERATOR_YML)
	@echo "Generating $(OUTPUT_SNMP_YML) for Cisco devices..."
	$(GENERATOR) generate \
		-m $(LOCAL_MIBS) \
		-m $(COMMON_MIBS) \
		-g $(GENERATOR_YML) \
		-o $(OUTPUT_SNMP_YML)

clean:
	@echo "Cleaning generated files..."
	rm -f $(OUTPUT_SNMP_YML)