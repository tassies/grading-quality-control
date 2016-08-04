# grading-quality-control
using weight, height, width, smoothness, and function to determine the quality of an object.
The scoring process is performed as follows:
• Each criterion value is entered as a whole numbered percentage in the range [0, 100]
• Each weight (one per criterion) is entered in as a real number in the range [0.0, 1.0]
◦ The sum of the weights must not be greater than 1.0
• The weights are each multiplied with their associated criterion and summed together


#include <iostream>

using namespace std;

int main()
{
    //criterion value as a percentage
    double widthPercentage = 0;
    double heightPercentage = 0;
    double smoothnessPercentage = 0;
    double functionPercentage = 0;
    double weightPercentage = 0;
    
    //weight criterion as a real number
    double weightWidth = 0;
    double weightHeight = 0;
    double weightSmoothness = 0;
    double weightFunction = 0;
    double weightWeight = 0;
    
    cout << "please enter the percentage of width between [0 ; 100] " << endl;
    cin >> widthPercentage;
    cout << "please enter the percentage of height [0 ; 100] " << endl;
    cin >> heightPercentage;
    cout << "please enter the percentage of smoothness [0 ; 100] " << endl;
    cin >> smoothnessPercentage;
    cout << "please enter the percentage of function [0 ; 100] " << endl;
    cin >> functionPercentage;
    cout << "please enter the percentage of the weight [0 ; 100] " << endl;
    cin >> weightPercentage;
    
    cout << "please enter the weight of the width [0.0 ; 1.0] " << endl;
    cin >> weightWidth;
    cout << "please enter the weight of the height [0.0 ; 1.0] " << endl;
    cin >> weightHeight;
    cout << "please enter the weight of the smoothness [0.0 ; 1.0] " << endl;
    cin >> weightSmoothness;
    cout << "please enter the weight of the function [0.0 ; 1.0] " << endl;
    cin >> weightFunction;
    cout << "please enter the weight of the weight [0.0 ; 1.0] " << endl;
    cin >> weightWeight;
    
    double sum = weightWidth + weightHeight + weightSmoothness + weightFunction + weightWeight;
    char SumOfWeight = (sum == 1) ? 'Y': 'N';
    cout << "Sum of weight = 1?: " << SumOfWeight << endl ;
    
    //cheking if the sum of the weights is not greater than 1.0
    if (sum < 1 )
    {
        cout << "error please enter the correct values" <<endl ;
    }
    else if (sum > 1)
    {
        cout << "error please enter the correct values" << endl;
        return -1;
    }
    double widthPercentageWidth = 0;
    double heightPercentageHeight = 0;
    double smoothnessPercentageSmoothness = 0;
    double functionPercentageFunction = 0;
    double weightPercentageWeight = 0;
    
    // weights multiplied with their associated criterion
    widthPercentageWidth = widthPercentage * weightWidth;
    heightPercentageHeight = heightPercentage * weightHeight;
    smoothnessPercentageSmoothness = smoothnessPercentage * weightSmoothness;
    functionPercentageFunction = functionPercentage * weightFunction;
    weightPercentageWeight = weightPercentage * weightWeight;
    
    //multiplied are summed together
    double total ;
    total = widthPercentageWidth +
    heightPercentageHeight +
    smoothnessPercentageSmoothness +
    functionPercentageFunction +
    weightPercentageWeight;
    
    //grading
    int grades = 0.0;
    grades = total;
    switch (grades / 10)
    {
    case 0:
    case 1:
    case 2:
    case 3:
    case 4:
        cout << " The product may not be sold " << endl;
        break;
    case 5:
        cout << " The product is sold at a normal price " << endl;
        break;
    case 6:
        cout << " The product is sold at a small mark-up " << endl;
        break;
    case 7:
        cout << " The product is sold at a small mark-up " << endl;
        break;
    case 8:
    case 9:
    case 10:
        cout << " The product is sold at a large mark-up " << endl;
        break;
    default:
        cout << " The product is sold at a normal price " << endl;
    }
    return 0;
}
