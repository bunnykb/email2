 #include <string>
    #include <iostream>
    #include <vector>
    #include "SubdomainPart.h"
    #include "TldPart.h"
    	using namespace std;
     
    	class DomainPart
    	{
     
    	public:
     
    	    // Default constructor (must have).
    	    DomainPart();
    	    // Set method plays the role of the init-constructor.
    	    void Set(const string& address);
    	    // Performs the validation.
    	    bool isValid();
    	private:
    	    string Address;
    	    vector<SubdomainPart> Subdomains;
    	    TldPart Tld;
     
     
    	    // Splits the domain into subdomains.
     
    	    bool Parse();
     
    	    bool SubdomainsAreValid();
     
    	};
