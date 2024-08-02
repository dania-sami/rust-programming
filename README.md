// DAY ONE OF EXPLORING RUST BLOCKCHAIN FRAMEWORKS
struct Company {
    name: String,
    ceo: String,
    interns: Vec<String>,
}

impl Company {
    // Create a new Company instance
    fn new(name: &str, ceo: &str, interns: Vec<&str>) -> Self {
        Company {
            name: name.to_string(),
            ceo: ceo.to_string(),
            interns: interns.into_iter().map(|s| s.to_string()).collect(),
        }
    }

    // Display company information
    fn display_info(&self) {
        println!("Company: {}", self.name);
        println!("CEO: {}", self.ceo);
        println!("Interns:");
        for intern in &self.interns {
            println!(" - {}", intern);
        }
    }
}

fn main() {
    // Create a list of intern names
    let intern_names = vec!["Alaa", "Dania", "Denys", "Ibrahim", "Serhi", "Usama"];

    // Create a new Company instance
    let flower_work = Company::new("FlowerWork", "Francisco", intern_names);

    // Display the company information
    flower_work.display_info();
}
