---
title: Contributing to TOSA software
permalink: /tosa/software.html
keywords:
    - TOSA
    - Machine Learning
jumbotron:
  title: TOSA Related Software
  description: TOSA related software projects
  image: /assets/images/content/ml-banner.jpg
flow:
  - row: container_row
    sections:
      - format: text
        text_content:
          text: |-
            # Description of the TOSA related software pieces on MLPlatform

            ### TOSA Reference Model & Test Generator
            In addition to the TOSA specification document, there is also a reference model written as C code which implements the exact behaviour as set out in the specification.
            This reference implementation is intended to be the “golden reference” for other TOSA implementations to be compared against and incorporated into regression test suites and such.
            The reference model consumes a FlatBuffers serialization of the network subgraph generated by the TOSA Serialization Library, along with input tensors for placeholder nodes in NumPy format.
            By default, the model validates and evaluates the network subgraph, and writes out the resulting output tensors in NumPy format.
            Alongside the TOSA Reference Model there is also a comprehensive set of tools for generating unit tests which exercise the behaviour of the TOSA operators.
            The tests are created as TOSA operations serialized in the flatbuffer format with inputs created in files using the NumPy format, as used by the reference model.

            For details on how to build and use the TOSA Reference Model, review the README.md in the root of that repo.

            ### TOSA MLIR Translator
            The TOSA MLIR translator repository [https://git.mlplatform.org/tosa/tosa_mlir_translator.git](https://git.mlplatform.org/tosa/tosa_mlir_translator.git) contains an MLIR pass which can serialize MLIR TOSA dialect content into a TOSA flatbuffer file.
            For details on how to build and use the TOSA MLIR translator, see the README.md in the root of that repository.

            ### TOSA Checker
            The TOSA Checker is a tool that provides with an easy way to ensure that a neural network model is compatible with the TOSA specification. The checker validates if the model can be expressed using exclusively TOSA primitive operators. It currently supports TensorFlow™ Lite models, support for additional model types will be added in the future.

            The Git repository containing the TOSA Checker is here: [https://git.mlplatform.org/tosa/tosa_checker.git](https://git.mlplatform.org/tosa/tosa_checker.git).

            Python packages are available on PyPi: [https://pypi.org/project/tosa-checker](https://pypi.org/project/tosa-checker).

            {:.table}
            | Repository | URL | Description |
            | ---------- | --- | ----------- |
            | Conformance Test Suite | [https://git.mlplatform.org/tosa/conformance_tests.git/](https://git.mlplatform.org/tosa/conformance_tests.git/) | Conformance tests for the Base Inference profile |
            | Reference Model | [https://git.mlplatform.org/tosa/reference_model.git/](https://git.mlplatform.org/tosa/reference_model.git/) | Reference implementation and testing infrastructure for TOSA |
            | Serialization Library | [https://git.mlplatform.org/tosa/serialization_lib.git/](https://git.mlplatform.org/tosa/serialization_lib.git/) | Methods to read and write serialized TOSA graphs using a flatbuffer schema |
            | TOSA Checker | [https://git.mlplatform.org/tosa/tosa_checker.git/](https://git.mlplatform.org/tosa/tosa_checker.git/) | Checks if a TensorFlow Lite model is compatible with the TOSA specification |
            | TOSA MLIR Translator | [https://git.mlplatform.org/tosa/tosa_mlir_translator.git/](https://git.mlplatform.org/tosa/tosa_mlir_translator.git/) | Uses the serialization library to convert a TOSA MLIR graph to a serialized flatbuffer |


---
