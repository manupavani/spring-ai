# Simple Java + Spring Boot + OpenAI Chatbot

A minimal chatbot with:

- Java 21
- Spring Boot
- Maven
- Simple HTML/JavaScript UI
- OpenAI Responses API

## 1. Set your OpenAI API key

### Windows PowerShell

```powershell
$env:OPENAI_API_KEY="your-api-key"
```

### Windows CMD

```cmd
set OPENAI_API_KEY=your-api-key
```

### Linux / macOS

```bash
export OPENAI_API_KEY="your-api-key"
```

## 2. Start the application

From the project directory:

```bash
mvn spring-boot:run
```

Or build it:

```bash
mvn clean package
java -jar target/openai-chatbot-0.0.1-SNAPSHOT.jar
```

## 3. Open the chatbot

Open:

http://localhost:8080

## How it works

Browser
   |
   | POST /api/chat
   v
Spring Boot ChatController
   |
   v
OpenAIService
   |
   | HTTPS
   v
OpenAI Responses API

The API key stays on the server and is not exposed to the browser.

Note: The sample sends each message independently. It does not maintain conversation history yet.
