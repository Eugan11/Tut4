# Tut4

#include <iostream>
#include <string>

using namespace Microsoft::VisualStudio::CppUnitTestFramework;

namespace UnitTest
{		
test(stacktest){
public:

method(createstacktest){
Assert::AreEqual(1, 1);}
		
testmethod(PushTest){
CStack TestStack(10);
int pushval = 10;
bool result;

result = TestStack.Push(pushval);
Assert::AreEqual(result, true);}

testmethod(PopTest){
CStack TestStack(10);
int pushval = 10;
int popval;
bool result;

result = TestStack.Push(pushval);
result = TestStack.Pop(popval);
Assert::AreEqual(result, true);
Assert::AreEqual(popval, pushval);}

testmethod(PopEmptyTest){
CStack TestStack(10);
int popval;
bool result;

result = TestStack.Pop(popval);
Assert::AreEqual(result, false);}
TEST_METHOD(PushFullTest){
CStack TestStack(10);
bool result;

for (int i = 0; i < 10; i++){
TestStack.Push(i);}
result = TestStack.Push(10);
Assert::AreEqual(result, false);}
};
}
			
