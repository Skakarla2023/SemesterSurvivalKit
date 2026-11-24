# Reranking

- Reranking is the process of reordering documents retrieved during the first search based on their relevance to user's query.
- The first retrieval system finds a set of possible documents.
- A reranker then examines this documents carefully and rearranges them by placing most relevant documents at the top.


<img width="515" height="237" alt="image" src="https://github.com/user-attachments/assets/53fe3eb5-d4e7-4931-a47c-0a7de8de561d" />


<img width="453" height="236" alt="image" src="https://github.com/user-attachments/assets/33acb9db-262f-4406-a83c-115202b50e31" />


<img width="395" height="165" alt="image" src="https://github.com/user-attachments/assets/f7e79087-a1a0-436d-a47a-3fa5cfb7fb17" />

### How does Reranking work?

1. The user enters a query.
2. A retrieval model retrieves a set of candidate documents.
3. A reranker receives the query and each candidate document.
4. It calculates a relevance score.
5. Documents are sorted based on their scores.
6. The best-ranked documents are passed to the LLM or displayed to the user.


<img width="550" height="260" alt="image" src="https://github.com/user-attachments/assets/bcefc0b5-55b1-4a9a-9157-c1ec9e795aa2" />


<img width="529" height="148" alt="image" src="https://github.com/user-attachments/assets/09eeb64c-1d35-4834-9186-46fcb206c50b" />
