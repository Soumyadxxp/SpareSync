# Spare Sync

Spare Sync is a web-based motorcycle spare-parts compatibility platform that helps users determine whether components from one motorcycle model are compatible with another.

The application combines a rule-based compatibility engine, natural-language part discovery, voice interaction, and a marketplace interface in a responsive single-page web application.

## Features

### Parts Compatibility Checker

The compatibility checker allows users to:

* Select a source motorcycle.
* Select a target motorcycle.
* Choose from 52 supported spare parts.
* Compare relevant technical specifications.
* Generate a compatibility percentage.
* View individual matching and non-matching criteria.
* Handle model-specific components such as ECUs separately.

### Intelligent Compatibility Assistant

The built-in assistant processes natural-language queries related to motorcycles and spare parts.

It supports:

* Motorcycle model detection.
* Spare-part detection.
* Fuzzy text matching.
* Partial names and spelling variations.
* Compatibility recommendations.
* Ranking of compatible motorcycle models.

Example queries:

```text
My bike is Classic 350
I have an NS200
Front disc compatibility
ECU compatibility
```

### Voice Interaction

The application supports browser-based voice input, allowing users to interact with the compatibility assistant using speech.

Voice functionality depends on browser support for the Web Speech API.

### Parts Marketplace

The marketplace interface allows users to:

* Create spare-part listings.
* Enter part specifications and descriptions.
* Set a selling price.
* Add seller contact information.
* Upload up to three product images.
* Browse available listings.
* Contact sellers through the built-in messaging interface.

### Responsive User Interface

The application includes:

* Responsive layouts for desktop and mobile devices.
* Animated application startup.
* Interactive compatibility analysis.
* Visual compatibility scores.
* Floating assistant interface.
* Tab-based navigation.
* Dynamic marketplace listings.

## Technology Stack

* HTML5
* CSS3
* JavaScript
* Web Speech API
* Browser DOM APIs
* Client-side data processing

The current implementation does not require an external framework, package manager, or build system.

## Application Architecture

Spare Sync is currently implemented as a client-side single-page application.

```text
spare-sync/
├── index.html
└── README.md
```

The main HTML file contains:

* Application markup.
* Responsive styling.
* Motorcycle and spare-parts datasets.
* Compatibility calculation logic.
* Natural-language query processing.
* Voice interaction logic.
* Marketplace functionality.
* User interface event handling.

## Compatibility Engine

The compatibility engine compares technical attributes between the selected source and target motorcycles.

Depending on the selected component, the system may evaluate properties such as:

* Engine displacement.
* Cooling system.
* Front disc size.
* Wheel size.
* Chain specification.
* ABS configuration.
* Fork type.
* Brake configuration.
* ECU code.

Each spare part is associated with a set of relevant compatibility criteria. The application compares these criteria and calculates a percentage-based compatibility score.

The result is classified into one of the following categories:

* Fully Compatible
* Partial Compatibility
* Not Compatible

Model-specific electronic components, such as ECUs and CDI units, receive additional compatibility restrictions.

## Supported Data

The current application dataset contains:

* 26 motorcycle models.
* 52 spare-part categories.
* Multiple mechanical and electronic compatibility parameters.

The supported motorcycles include models from manufacturers such as:

* Royal Enfield
* Bajaj
* KTM
* TVS
* Yamaha
* Suzuki
* Honda
* Benelli
* Kawasaki
* BMW
* Hero

Supported spare parts include braking components, suspension components, engine parts, electrical components, transmission parts, wheels, filters, sensors, and other common motorcycle components.

## Getting Started

### Prerequisites

A modern web browser is required.

Recommended browsers include:

* Google Chrome
* Microsoft Edge
* Mozilla Firefox


## Usage

### Checking Part Compatibility

1. Open the Compatibility tab.
2. Select the source motorcycle.
3. Select the target motorcycle.
4. Select the spare part.
5. Click `ANALYZE COMPATIBILITY`.
6. Review the compatibility score and technical comparison.

### Using the Compatibility Assistant

First, provide the motorcycle model:

```text
My bike is NS200
```

Then ask about a component:

```text
Front disc compatibility
```

The assistant analyzes the selected motorcycle and returns compatible alternatives based on the stored technical specifications.

### Creating a Marketplace Listing

1. Open the Marketplace tab.
2. Select `SELL PART`.
3. Enter the part details.
4. Add the price and seller information.
5. Upload product images if required.
6. Publish the listing.

## Limitations

The current version is primarily a client-side prototype.

The following data is not persisted after the browser session unless additional storage or backend functionality is implemented:

* Marketplace listings.
* User information.
* Chat messages.
* Application state.

The compatibility assistant uses locally implemented matching and rule-based processing rather than an external machine-learning or large language model API.

## Disclaimer

Compatibility results are based on the technical specifications stored in the application's internal dataset.

Actual part compatibility may also depend on:

* Model year.
* Motorcycle generation.
* OEM part numbers.
* Mounting dimensions.
* Electrical connectors.
* Wiring configurations.
* Regional model variations.
* Aftermarket modifications.

Compatibility should be verified with the manufacturer, an authorized service center, or a qualified mechanic before purchasing or installing a component.
---



Spare Sync provides a unified interface for motorcycle part compatibility analysis, intelligent part discovery, and spare-parts marketplace functionality.
