# Flutter Language Translator App with Quiz Feature

This update adds a new gamification feature to the Language Translator app in the form of quizzes powered by Azure OpenAI (ready for integration). The quiz feature helps users practice and test their language knowledge while earning XP and maintaining daily streaks.

## Quiz Feature Implementation

The quiz feature is implemented with the following components:

### Models
- `Quiz`: Represents a quiz with multiple questions
- `QuizItem`: Individual quiz questions of different types (multiple choice, fill-in-blank, listening, OCR)
- `QuizResult`: Stores results of completed quizzes
- `UserQuizData`: Tracks user progress, XP, level, and streaks

### Service
- `QuizService`: Manages quiz data, user progress, and quiz results
- Currently uses mock data for development
- Ready for Azure OpenAI integration when server is available

### UI Components
- `QuizHomeScreen`: Entry point with user stats and quiz options
- `QuizScreen`: Interactive quiz interface with various question types
- `QuizResultScreen`: Shows quiz results and rewards
- `QuizNavButton`: Navigation component to access quizzes from main UI

## How to Use

1. Add the `QuizNavButton` to your main UI
2. Add `QuizService` to your provider tree (see `main_with_quiz.dart`)
3. Update your theme provider with dark/light mode functionality
4. To start a quiz, navigate to the Quiz Home Screen and select a language pair

## Integration with Azure OpenAI

The quiz feature is designed to work with Azure OpenAI for dynamic quiz generation. The implementation includes:

1. Ready-to-use API client structure in `QuizService`
2. Support for different question types that can leverage AI capabilities
3. Local grading that can be replaced with server-side validation

To connect to Azure OpenAI:
1. Set up your Azure OpenAI service
2. Update the API endpoint and key in `QuizService`
3. Uncomment the API call sections in the service

## Features

- User progression system with XP and levels
- Daily streaks to encourage regular practice
- Different quiz question types
- Quiz history tracking
- Detailed results with feedback
- Support for multiple language pairs
- Compatible with dark/light mode

This implementation focuses on the client-side components first, allowing for immediate testing and UI feedback while the server-side components are being developed.
