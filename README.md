# skyhookers
Evaluating Blockchain as a Service for E-Voting
<h3>ELECTION CREACTION</h3> Election administrators create election ballots using a decentralized app(dApp). This decentralized app interacts with an election creation smart
 contract, in which the administrator defines a list of candidates and voting districts. This smart contract creates a set of ballot smart contracts and deploys them onto the
 blockchain, with a list of the candidates, for each voting district, where each voting district is a parameter in each ballot smart contract. When the election is created,
 each corresponding district node is given permission to interact with his corresponding ballot smart contract

<h3>VOTER REGISTRATION</h3> The registration of voter phase is
conducted by the election administrators. When an election is created the election administrators must define
a deterministic list of eligible voters. This requires a
component for a government identity verification service
to securely authenticate and authorize eligible individuals. Using such verification services, each of the eligible
voter should have an electronic ID and PIN number and
information on what voting district the voter is located
in. For each eligible voter, a corresponding wallet would
be generated for the voter. The wallet generated for each
individual voter should be unique for each election the
voter is eligible for and a NIZKP could be integrated to
generate such wallet so that the system itself does not
know which wallet matches an individual voter.

<h3>VOTE TRANSACTION</h3> When an individual votes at a voting
district, the voter interacts with a ballot smart contract
with the same voting district as is defined for any
individual voter. This smart contract interacts with the
blockchain via the corresponding district node, which appends the vote to the blockchain if consensus is reached
between the majority of the corresponding district nodesEach vote is stored as a transaction on the blockchain
whereas each individual voter receives the transaction
ID for their vote for verifying purposes (see “Verifying
vote” section). Each transaction on the blockchain holds
information about whom was voted for, and the location
of aforementioned vote. Each vote is appended onto the
blockchain by its corresponding ballot smart contract, if
and only if all corresponding district nodes agree on the
verification of the vote data. When a voter casts his vote,
the weight of their wallet is decreased by 1, therefore
not enabling them to vote more than once per election. a single transaction on the
public Ethereum blockchain includes the transaction ID,
the block which the transaction is located, the age of
the transaction, the wallet which sent the transaction
and who received it, the total value which was sent
and the transaction fee. A transaction in our proposed
system doesn’t require all of this information, a single
transaction only has information of the transaction ID,
the block which the transaction is located at, to which
smart contract the transaction was sent, Finally the value of the transaction is the data
which was selected to cast, A transaction in our system . therefore
reveals no information about the individual voter who
casted this particular vote. The age of a single transaction
is excluded to protect individual voters from a timing
attack

<h3>TALLYING RESULTS</h3> The tallying of the election is done on
the fly in the smart contracts. Each ballot smart contract
does their own tally for their corresponding location in
its own storage. When an election is over, the final result
for each smart contract is published.
