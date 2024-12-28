graph TD
    A[Start] --> B{Main Menu}
    B -->|1| C[Admin Panel]
    B -->|2| D[User Panel]
    B -->|3| E[Branch List & Contacts]
    B -->|4| F[Exit]

    C -->|Enter Passcode| C1{Validate Admin}
    C1 -->|Valid| C2[Admin Menu]
    C1 -->|Invalid| B
    
    C2 -->|1| CA[View All Accounts]
    C2 -->|2| CB[Delete Account]
    C2 -->|3| CC[Manage Loans]
    C2 -->|4| B
    
    CC -->|1| CC1[Loan with Interest]
    CC -->|2| CC2[Loan with Collateral]
    CC -->|3| CC3[View Loan Details]
    CC -->|4| C2

    D -->|User Options| D1{Account Type}
    D1 -->|1| DA[Open Regular Account]
    D1 -->|2| DB[Open Student Account]
    D1 -->|3| DC[Login]
    D1 -->|4| B

    DC -->|Enter Credentials| DC1{Validate Login}
    DC1 -->|Valid| D2[User Menu]
    DC1 -->|Invalid| D1

    D2 -->|1| D2A[Show Account Details]
    D2 -->|2| D2B[View Balance]
    D2 -->|3| D2C[Deposit Money]
    D2 -->|4| D2D[Withdraw Money]
    D2 -->|5| D2E[Transfer Money]
    D2 -->|6| D2F[Set Saving Goals]
    D2 -->|7| D2G[Online Payment]
    D2 -->|8| D1

    D2C -->|Options| D2C1{Deposit Type}
    D2C1 -->|1| D2CA[Without Interest]
    D2C1 -->|2| D2CB[With Interest]

    E --> B

    style A fill:#f9f,stroke:#333,stroke-width:2px
    style B fill:#bbf,stroke:#333,stroke-width:2px
    style C fill:#dfd,stroke:#333,stroke-width:2px
    style D fill:#dfd,stroke:#333,stroke-width:2px
    style E fill:#ffd,stroke:#333,stroke-width:2px
    style F fill:#fdd,stroke:#333,stroke-width:2px
