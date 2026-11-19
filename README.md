# V-to-C-Annotation-Conversion
This project aims to transfer annotated whole-slide images and their associated XML annotation files from V to C while preserving annotation geometry and ensuring accurate alignment with the corresponding image coordinates.

## 1. Project Overview

This project aims to develop a Python-based solution to transfer whole-slide images (.svs) and their associated XML annotations from VIPER to Concentriq LS while preserving annotation geometry, coordinates, and alignment with the original images.

## 2. Project Scope

The project focuses on converting VIPER annotation data into a format compatible with Concentriq LS without modifying the original SVS image data.

### In Scope:

- Read and parse XML annotation files exported from VIPER.
- Extract annotation information, including coordinates, shapes, labels, and identifiers.
- Map VIPER annotation coordinates to the corresponding SVS image coordinate system.
- Transform annotation data into a format supported by Concentriq LS (XML, JSON, or API payload, subject to verification).
- Validate annotation accuracy, geometry, and alignment with the original images.
- Test the converted annotations in a Concentriq LS test environment, if access is available.

### Out of Scope:

- Modifying or re-encoding original SVS image files.
- Changing the scientific interpretation of annotations.
- Developing a new whole-slide image viewer.
- Integrating with production systems during initial development.

## 3. Project Deliverables

Deliverable
Description
Python conversion script
Reads VIPER XML and transforms annotation data into the verified Concentriq-compatible format.
Annotation mapping specification
Documents source and target fields, coordinate systems, and conversion rules.
Validation script
Checks annotation counts, coordinates, geometry, and image alignment.
Synthetic test dataset
Contains sample annotation files and corresponding test image information without patient data.
Test results
Documents conversion accuracy, errors, and limitations.
GitHub repository
Contains source code, documentation, test cases, and version history.

## 4. Development Phases

### Phase 1 — Analyze Source Data
    Examine the VIPER XML structure and identify annotation types, coordinates, labels, and image references.
### Phase 2 — Define Conversion Requirements
    Verify Concentriq LS annotation import capabilities and establish field mappings and coordinate transformation rules.
### Phase 3 — Develop Python Converter
    Implement XML parsing, annotation transformation, and output generation.
### Phase 4 — Validate and Test
    Verify annotation integrity, coordinate accuracy, and alignment with the corresponding SVS images.
### Phase 5 — Integration Testing
    Test annotation import into an authorized Concentriq LS test environment and document the results.

## 5. Success Criteria

The project will be considered successful when:
- All supported VIPER annotations are converted without unintended data loss.
- Annotation coordinates and geometry are preserved or correctly transformed.
- Converted annotations align with the intended regions of the corresponding SVS images.
- Validation identifies missing, unsupported, or incorrectly converted annotations.
- The converted files can be successfully imported into Concentriq LS using a verified, supported method.

## 6. Technology Stack

Python: XML parsing, data transformation, and validation.
XML / JSON: Annotation data exchange formats.
SVS: Whole-slide image format.
Git: Source code version control.
GitHub: Project documentation and source code repository.
Concentriq LS: Target digital pathology platform.
