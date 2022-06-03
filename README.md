# AirlinesCustomerSegmentation

Use airline customer data to classify customers, analyse characteristics of different customer categories, compare customer values of different customer categories, provide personalized services to customer categories of different values, and formulate a corresponding marketing strategy.

RFM: Recency, Frequency, and Monetary Using the RFM concept as shown above in performing feature selection:

Recency -> column LAST_TO_END (Distance from last flight time to last flight order)
Frequency -> column FLIGHT_COUNT (Number of customer flights) 
Monetary -> column SEG_KM_SUM (For the monetary column, as an adjustment in the airline business, this feature is replaced by accumulated flight hours within a certain period of time)

Then there are also columns that are considered important in assessing customer value in the aviation business, namely: Loyalty -> column MEMBER_DURATION (Membership length, which reflects whether the member is an existing customer) Cabin -> column avg_discount (Discount factor related to cabin class, reflecting high and low customer value)

These columns will be used in the clustering process

When k takes a value of 4, the cluster performance is not obvious in terms of membership time and average discount rate, and the clustering effect is not optimal.

When the value of k is 5, the analysis result is more reasonable, and the five types of people divided have their own characteristics and do not repeat each other.

Cluster 0 (blue)(24103 members):

    Passenggers who have low discount that customers get (average)
    Passenggers who have Low Total distance (km) flights that have been done
    Passengger who have low Number of customer flights
    Passengger who have low last flight time to last flight order interval
    Passengger who have high member duration. Cluster 0 is passenggers who is long time member.

They may have taken a few flights and have not taken the airline ’s plane again. They are considered lost customers. You should try to grasp the latest information of these customers, maintain interaction with customers, and adopt certain marketing methods such as preferential measures and cross-selling to restore such customers.

Cluster 2 (Red) (15366 members):

    Passenggers who have Medium discount that customers get (average)
    Passenggers who have High Total distance (km) flights that have been done
    Passengger who have High Number of customer flights
    Passengger who have low last flight time to last flight order interval
    Passengger who have medium member duration. Cluster 2 is Frequent Flyer passenggers. This type of customer is a high-value customer, generally a high-end customer Business personnel in the cabin are the key to maintaining and developing, and can adopt relevant preferential policies such as member upgrade measures to increase their number of rides.

Cluster 4 (Yellow) (11888 members):

    Passenggers who have High discount that customers get (average)
    Passenggers who have low Total distance (km) flights that have been done
    Passengger who have low Number of customer flights
    Passengger who have high last flight time to last flight order interval
    Passengger who have low member duration. Cluster 4 is customer who fly due to discount program. It is usually an occasional consumption, which may be due to seasonal reasons or related to promotional activities. For such users, it is necessary to maintain and stimulate consumption as much as possible.

Cluster 3 (Cyan) (5263 members):

    Passenggers who have Low discount that customers get (average)
    Passenggers who have low Total distance (km) flights that have been done
    Passengger who have low Number of customer flights
    Passengger who have high last flight time to last flight order interval
    Passengger who have low member duration. Cluster 3 is passengers who used our flight lately. Need to maintain well, you can also use member upgrade measures.

Cluster 1 (Green) (4809 members):

    Passenggers who have Low discount that customers get (average)
    Passenggers who have Low Total distance (km) flights that have been done
    Passengger who have low Number of customer flights
    Passengger who have low last flight time to last flight order interval
    Passengger who have short member duration. Cluster 1 is passenggers who doesnt interested with the company flight (flight rarely) It has low data in all aspects and belongs to low-value users. For these users, they should be maintained as much as possible, and then stimulate their consumption to stimulate their consumption vitality.

Conclusion:

    The highest cluster passenger may have taken a few flights and have not taken the airline ’s plane again. They are considered lost customers. You should try to grasp the latest information of these customers, maintain interaction with customers, and adopt certain marketing methods such as preferential measures and cross-selling to restore such customers.
    Airflight is a high-value customer, generally a high-end customer Business personnel in the cabin are the key to maintaining and developing, and can adopt relevant preferential policies such as member upgrade measures to increase their number of rides.
    Many new customer/passenger is customer who fly due to discount program. It is usually an occasional consumption, which may be due to seasonal reasons or related to promotional activities. For such users, it is necessary to maintain and stimulate consumption as much as possible.
    There are passenger who used our flight lately. Need to maintain well, you can also use member upgrade measures.
    There are few number of passenger has low data in all aspects and belongs to low-value users. For these users, they should be maintained as much as possible, and then stimulate their consumption to stimulate their consumption vitality.

