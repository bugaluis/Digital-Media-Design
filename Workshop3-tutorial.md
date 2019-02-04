//ViewController

import UIKit
import CoreLocation

// Inside of the ViewController

class ViewController: UIViewController {

    let locationManager = CLLocationManager ()
    
    
      @IBOutlet weak var labellocation: UILabel!
    
    
    
    
    override func viewDidLoad() {
        super.viewDidLoad()
    
        locationManager.requestAlwaysAuthorization()
        locationManager.delegate = self
        locationManager.startUpdatingLocation()
        
        
        
        
        
    }

  
    
    
    
    
    
}

// Outside of the ViewController

extension ViewController: CLLocationManagerDelegate {
    
    func locationManager(_ manager: CLLocationManager, didUpdateLocations locations: [CLLocation]) {
        let location = locations.last!
        print(location.coordinate)
        labellocation.text = "\(location.coordinate.latitude) \(location.coordinate.longitude)"
        
        
        
        
    }
    
    
        

    }
    
 //location gpx
 
 <?xml version="1.0"?>
<gpx version="1.1" creator="Xcode">
    
    <!--
     Provide one or more waypoints containing a latitude/longitude pair. If you provide one
     waypoint, Xcode will simulate that specific location. If you provide multiple waypoints,
     Xcode will simulate a route visiting each waypoint.
     -->
    <wpt lat="-12.121480" lon="-77.017173"> </wpt>
    
    
       <wpt lat="-12.098721" lon="-76.996553"> </wpt>
       
          <wpt lat="-12.128322" lon="-77.002529"> </wpt>

        
</gpx>

 
 
