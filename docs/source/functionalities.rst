Функциональность Hyperledger Fabric
==================================

Hyperledger Fabric - это реализация распределенной технологии учёта (DLT - 
distributed ledger technology), готовой к использованию на уровне
корпоративных стандартов по сетевой безопасности, масштабируемости,
конфиденциальности и производительности, и представленной в модульной
архитектуре блокчейн (blockchain).
Hyperledger Fabric обеспечивает следующие функциональные особенности сетей, 
построенных на базе блокчейн технологий:

Управление идентификацией
-------------------

Чтобы использовать сети с выдачей разрешений на выполнение операций,
Hyperledger Fabric предоставляет службу идентификации участников сети, которая
управляет идентивикаторами пользователей (user IDs) и аутентифицирует всех
участников сети. Для предоставления дополнительных уровней доступа посредством
авторизации для специфических операций в сети, могут использоваться списки
контроля доступа. Нарпример указанному по ID пользователю может быть разрешен
запуск приложений, написанных на chaincode, но в тоже время ему заблокирована
возможность добавлять новые инструкции в такие приложения.

Privacy and confidentiality
---------------------------

Hyperledger Fabric enables competing business interests, and any groups that
require private, confidential transactions, to coexist on the same permissioned
network. Private **channels** are restricted messaging paths that can be used
to provide transaction privacy and confidentiality for specific subsets of
network members. All data, including transaction, member and channel
information, on a channel are invisible and inaccessible to any network members
not explicitly granted access to that channel.

Efficient processing
--------------------

Hyperledger Fabric assigns network roles by node type. To provide concurrency
and parallelism to the network, transaction execution is separated from
transaction ordering and commitment. Executing transactions prior to
ordering them enables each peer node to process multiple transactions
simultaneously. This concurrent execution increases processing efficiency on
each peer and accelerates delivery of transactions to the ordering service.

In addition to enabling parallel processing, the division of labor unburdens
ordering nodes from the demands of transaction execution and ledger
maintenance, while peer nodes are freed from ordering (consensus) workloads.
This bifurcation of roles also limits the processing required for authorization
and authentication; all peer nodes do not have to trust all ordering nodes, and
vice versa, so processes on one can run independently of verification by the
other.

Chaincode functionality
-----------------------

Chaincode applications encode logic that is
invoked by specific types of transactions on the channel. Chaincode that
defines parameters for a change of asset ownership, for example, ensures that
all transactions that transfer ownership are subject to the same rules and
requirements. **System chaincode** is distinguished as chaincode that defines
operating parameters for the entire channel. Lifecycle and configuration system
chaincode defines the rules for the channel; endorsement and validation system
chaincode defines the requirements for endorsing and validating transactions.

Modular design
--------------

Hyperledger Fabric implements a modular architecture to
provide functional choice to network designers. Specific algorithms for
identity, ordering (consensus) and encryption, for example, can be plugged in
to any Hyperledger Fabric network. The result is a universal blockchain
architecture that any industry or public domain can adopt, with the assurance
that its networks will be interoperable across market, regulatory and
geographic boundaries.

.. Licensed under Creative Commons Attribution 4.0 International License
   https://creativecommons.org/licenses/by/4.0/
