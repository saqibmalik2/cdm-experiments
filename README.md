# CDM Experiments - Derivatives Trade Modeling

Personal exploration of ISDA's Common Domain Model (CDM) and Rosetta DSL for standardized derivatives representation and lifecycle event processing.

## 🎯 Overview

This repository demonstrates practical implementations of CDM concepts including:
- Product definitions in Rosetta DSL for FX and rates derivatives
- FpML to CDM transformation patterns
- Trade lifecycle event modeling
- Data validation and business rule implementation

## 📁 Repository Structure

```
cdm-experiments/
├── rosetta/                    # Rosetta DSL model definitions
│   ├── products/              # Product type definitions
│   ├── events/                # Lifecycle event models
│   └── functions/             # Validation and transformation functions
├── src/
│   └── main/java/com/cdm/
│       ├── mapper/            # FpML ↔ CDM transformation
│       ├── validator/         # Trade validation logic
│       └── examples/          # Usage examples
├── data/
│   ├── fpml-samples/          # Sample FpML documents
│   └── cdm-samples/           # CDM JSON representations
└── docs/                      # Technical notes and learnings
```

## 🔧 Technologies

- **Rosetta DSL** - Domain modeling language for CDM definitions
- **Java 17** - Implementation and integration code
- **FpML 5.x** - Financial Products Markup Language standard
- **JUnit 5** - Testing framework
- **Maven** - Build and dependency management

## 🚀 Key Examples

### Interest Rate Swap Definition
Complete Rosetta DSL model for vanilla IRS including:
- Fixed and floating leg specifications
- Calculation period and payment date logic
- Day count conventions and business day adjustments
- Validation rules ensuring structural integrity

### FX Forward Modeling
FX Forward product definition with:
- Settlement date calculations
- Currency pair specifications
- Value date adjustments for holidays

### FpML Transformation
Java utilities demonstrating:
- Parsing FpML 5.x documents
- Mapping to CDM type structure
- Handling optional fields and defaults
- Validation of transformed trades

### Lifecycle Event Processing
Examples of modeling:
- Trade execution and booking
- Novation (transfer of obligations)
- Amendment and modification
- Early termination

## 📚 Learning Focus Areas

### Data Standardization Challenges
- Handling proprietary format variations across institutions
- Mapping ambiguous or optional fields
- Maintaining semantic equivalence during transformation
- Validation rule implementation

### Type-Safe Domain Modeling
- Leveraging Rosetta's strong typing
- Implementing business constraints as conditions
- Function composition for complex validation
- Generated code inspection and usage patterns

### Regulatory Reporting
- Understanding DRR (Digital Regulatory Reporting) extension
- Mapping CDM to regulatory formats (EMIR, Dodd-Frank)
- Capturing required fields for compliance

## 🎓 References & Resources

- [FINOS CDM GitHub](https://github.com/finos/common-domain-model) - Official CDM repository
- [Rosetta DSL Documentation](https://docs.rosetta-technology.io/) - Language specification
- [ISDA CDM Portal](https://www.isda.org/2020/06/08/isda-common-domain-model/) - CDM overview and use cases
- [FpML Standards](https://www.fpml.org/) - FpML specification and examples

## 🏗️ Build Instructions

```bash
# Clone repository
git clone https://github.com/saqibmalik2/cdm-experiments.git
cd cdm-experiments

# Build project (requires Java 17+)
mvn clean install

# Run example transformations
mvn exec:java -Dexec.mainClass="com.cdm.examples.FpmlToCdmExample"

# Run tests
mvn test
```

## 📝 Current Status

**Phase 1: Foundation** ✅
- Core product definitions (IRS, FX Forward, FX Option)
- Basic FpML parsing and transformation
- Validation framework

**Phase 2: In Progress** 🚧
- Extended lifecycle event coverage
- Advanced validation rules
- Collateral management integration points

**Phase 3: Planned** 📋
- DRR regulatory reporting examples
- Performance optimization for high-volume processing
- Integration with market data feeds

## 💡 Key Insights

Working with CDM has highlighted several important concepts:

1. **Standardization ≠ Simple** - Creating a universal model requires handling countless edge cases and variations
2. **Type Safety Matters** - Rosetta's strong typing catches errors at model definition time rather than runtime
3. **FpML Bridge** - Many firms still use FpML, so bidirectional transformation is crucial for adoption
4. **Event-Driven Architecture** - CDM's lifecycle event model aligns well with modern event sourcing patterns

## 📧 Contact

This is a personal learning project. Feel free to explore the code and examples.

**Note**: This repository is for educational and demonstration purposes. It references publicly available CDM specifications and does not contain proprietary trading system implementations.

---

*Last Updated: November 2025*
