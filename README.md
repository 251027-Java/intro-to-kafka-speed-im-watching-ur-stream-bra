# Pair Programming: CLI Chat App with Kafka

## The Mission
Work with a partner to build a real-time chat application using Kafka as the message broker.
**Roles:**
-   **Driver:** Types the commands/code.
-   **Navigator:** Reads the docs and guides the logic.
*Switch roles every 30 minutes.*

## Architecture
-   **Topic:** `global-chat`
-   **User A**: Produces messages to `global-chat`. Consumes from `global-chat` (filtering out their own messages if possible, or just seeing everything).
-   **User B**: Same.

## Steps
1.  **Infrastructure**: Spin up Kafka using Docker Compose.
2.  **Console Test**:
    -   Partner A opens a specific Terminal (The Producer).
    -   Partner B opens a specific Terminal (The Consumer).
    -   Verify you can chat.
3.  **Java Wrapper (Challenge)**:
    -   Write a simple Java Main class `ChatApp.java`.
    -   Use `Scanner` to read input and send to Kafka.
    -   Use a separate Thread to constantly poll Kafka and print incoming messages.
    -   *Result:* A terminal window where you can type and see other people's messages appear asynchronously.

## Definition of Done
-   Two distinct terminal windows running the Java app.
-   Message typed in Window A appears in Window B.
