CXX=g++
LD=ld
CXXFLAGS= -c -pthread -Wall -Wno-switch -Wno-unused-function -std=c++11 -fPIC
LDFLAGS = -shared -Llib -lbid
ROOT_DIR=.
BASE_SRC_DIR=${ROOT_DIR}
INCLUDES=-I${ROOT_DIR}
TARGET=libTwsSocketClient.so
SRCS =	ContractCondition.cpp          \
	Decimal.cpp                    \
	DefaultEWrapper.cpp            \
	EClient.cpp                    \
	EClientSocket.cpp              \
	EDecoder.cpp                   \
	EMessage.cpp                   \
	EMutex.cpp                     \
	EOrderDecoder.cpp              \
	EReader.cpp                    \
	EReaderOSSignal.cpp            \
	ESocket.cpp                    \
	executioncondition.cpp         \
	MarginCondition.cpp            \
	OperatorCondition.cpp          \
	OrderCondition.cpp             \
	PercentChangeCondition.cpp     \
	PriceCondition.cpp             \
	SoftDollarTier.cpp             \
	StdAfx.cpp                     \
	TimeCondition.cpp              \
	Utils.cpp                      \
	VolumeCondition.cpp            \

OBJS = ${SRCS:.cpp=.o}

$(TARGET): $(OBJS)
	$(LD) $(LDFLAGS) $* -o $@

$(OBJS): $(SRCS)
	$(CXX) $(CXXFLAGS) ${@:.o=.cpp} $(INCLUDES) -o $@

clean:
	rm -f $(TARGET) *.o

