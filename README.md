# SNHU-CS-230
# Draw It or Lose It - Game Management System

## Project Overview
This repository contains a multi-phase development project for The Gaming Room's "Draw It or Lose It" game platform, developed as part of CS 230 coursework. The project evolved from initial Java implementation focusing on design patterns to a comprehensive software design document addressing platform expansion requirements.

## Client and Software Requirements
The Gaming Room needed to expand their Android-based game "Draw It or Lose It" to a web-based platform. The game, similar to "Win, Lose or Draw", required:
* Multiple concurrent team support
* Unique game/team name validation
* Timed gameplay (four one-minute rounds)
* Progressive image rendering (30-second intervals)
* Cross-platform accessibility

## Development Highlights

### Phase 1: Core Implementation
Successfully implemented key Java components including:
* Singleton pattern in GameService class to ensure single game engine instance
* Iterator pattern for efficient game/team/player lookups
* Unique identifier management for games, teams, and players
* Unit testing through SingletonTester class

```java
// Singleton Implementation
private static GameService instance = null;

public static GameService getGameService() {
    if (instance == null) {
        instance = new GameService();
    }
    return instance;
}
```

### Phase 2: Security Implementation
Added authentication layer using Maven:
* Secure user session management
* Role-based access control
* Integration with web-based architecture

### Phase 3: Software Design Documentation
Developed comprehensive design documentation including:
* Detailed platform analysis (Windows, Linux, Mac, Mobile)
* System architecture recommendations
* Memory and storage management strategies
* Security considerations for web deployment

## Technical Achievements
The strongest aspects of this project include:
1. Clean implementation of design patterns
2. Thorough platform evaluation and recommendations
3. Consideration of scalability in design
4. Integration of security features

## Development Process Insights
The iterative development process proved valuable by:
* Starting with core Java implementation
* Adding security layers through Maven
* Expanding to full system architecture design
* Considering cross-platform deployment strategies

## Design Considerations
Key factors that influenced the design:
* Need for centralized game state management (Singleton pattern)
* Efficient data lookup requirements (Iterator pattern)
* Cross-platform compatibility
* Scalability for multiple concurrent games
* Security for web-based deployment

## Recommendations and Future Improvements
Areas identified for enhancement:
* Implement caching for improved performance
* Add load balancing for better scalability
* Enhance security features beyond basic authentication
* Implement real-time gameplay features
* Add persistent storage for game states

## Platform Recommendations
After careful analysis, Linux emerged as the recommended server platform due to:
* Cost-effectiveness
* Robust performance
* Strong security features
* Excellent support for web hosting
* Scalability options

## Getting Started

### Prerequisites
* Java JDK 8 or higher
* Maven (for authentication module)
* IDE supporting Java development

### Installation
1. Clone the repository
2. Import as Maven project
3. Run `mvn clean install`
4. Execute ProgramDriver class to test core functionality

## Testing
The project includes:
* SingletonTester for verifying GameService instance management
* Iterator pattern tests for data access
* Authentication module tests
