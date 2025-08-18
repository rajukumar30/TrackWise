# TrackWise — Per-class detailed explanation

Generated explanations for Java classes found in the backend. Use this as a guide — it's an automated summary that highlights key fields, methods, annotations, and likely responsibilities.

### `TrackWiseApplication.java` — *class*
- **Path:** `TrackWise-main/TrackWise-main/backend/src/main/java/org/godigit/trackwise/TrackWiseApplication.java`
- **Package:** `org.godigit.trackwise`
- **Class annotations:** `SpringBootApplication`

**Fields (approx.):** None detected or declared dynamically.

**Methods (approx.):**
- `main(...)` — `public static void main(String[] args) {` 

**Purpose (in plain words):**
- General-purpose class/DTO/utility — open the file to see exact responsibilities.

---

### `MailConfig.java` — *class*
- **Path:** `TrackWise-main/TrackWise-main/backend/src/main/java/org/godigit/trackwise/config/MailConfig.java`
- **Package:** `org.godigit.trackwise.config`
- **Class annotations:** `Configuration, Bean`
- **Detected role(s):** Configuration

**Fields (approx.):** None detected or declared dynamically.

**Methods (approx.):**
- `javaMailSender(...)` — `public JavaMailSender javaMailSender() {` Annotations: `Bean`

**Purpose (in plain words):**
- This is a Spring configuration class — beans, schedulers, or security rules are likely defined here.

---

### `SchedulerConfig.java` — *class*
- **Path:** `TrackWise-main/TrackWise-main/backend/src/main/java/org/godigit/trackwise/config/SchedulerConfig.java`
- **Package:** `org.godigit.trackwise.config`
- **Class annotations:** `Configuration, Bean`
- **Detected role(s):** Configuration

**Fields (approx.):** None detected or declared dynamically.

**Methods (approx.):**
- `taskScheduler(...)` — `public ThreadPoolTaskScheduler taskScheduler() {` Annotations: `Bean`

**Purpose (in plain words):**
- This is a Spring configuration class — beans, schedulers, or security rules are likely defined here.

---

### `SecurityConfig.java` — *class*
- **Path:** `TrackWise-main/TrackWise-main/backend/src/main/java/org/godigit/trackwise/config/SecurityConfig.java`
- **Package:** `org.godigit.trackwise.config`
- **Class annotations:** `Configuration, EnableWebSecurity, Bean`
- **Detected role(s):** Configuration

**Fields (approx.):** None detected or declared dynamically.

**Methods (approx.):**
- `securityFilterChain(...)` — `public SecurityFilterChain securityFilterChain(HttpSecurity http) throws Exception {` Annotations: `Bean`

**Purpose (in plain words):**
- This is a Spring configuration class — beans, schedulers, or security rules are likely defined here.

---

### `SwaggerConfig.java` — *class*
- **Path:** `TrackWise-main/TrackWise-main/backend/src/main/java/org/godigit/trackwise/config/SwaggerConfig.java`
- **Package:** `org.godigit.trackwise.config`
- **Class annotations:** `Configuration, Bean`
- **Detected role(s):** Configuration

**Fields (approx.):** None detected or declared dynamically.

**Methods (approx.):**
- `api(...)` — `public Docket api() {` Annotations: `Bean`

**Purpose (in plain words):**
- This is a Spring configuration class — beans, schedulers, or security rules are likely defined here.

---

### `WebConfig.java` — *class*
- **Path:** `TrackWise-main/TrackWise-main/backend/src/main/java/org/godigit/trackwise/config/WebConfig.java`
- **Package:** `org.godigit.trackwise.config`
- **Class annotations:** `Configuration, Override`
- **Detected role(s):** Configuration
- **Implements:** `WebMvcConfigurer`

**Fields (approx.):** None detected or declared dynamically.

**Methods (approx.):**
- `addCorsMappings(...)` — `public void addCorsMappings(CorsRegistry registry) {` Annotations: `Override`

**Purpose (in plain words):**
- This is a Spring configuration class — beans, schedulers, or security rules are likely defined here.

---

### `WebSocketConfig.java` — *class*
- **Path:** `TrackWise-main/TrackWise-main/backend/src/main/java/org/godigit/trackwise/config/WebSocketConfig.java`
- **Package:** `org.godigit.trackwise.config`
- **Class annotations:** `Configuration, EnableWebSocketMessageBroker, Override, Override`
- **Detected role(s):** Configuration
- **Implements:** `WebSocketMessageBrokerConfigurer`

**Fields (approx.):** None detected or declared dynamically.

**Methods (approx.):**
- `configureMessageBroker(...)` — `public void configureMessageBroker(MessageBrokerRegistry config) {` Annotations: `Override`
- `registerStompEndpoints(...)` — `public void registerStompEndpoints(StompEndpointRegistry registry) {` Annotations: `Override`

**Purpose (in plain words):**
- This is a Spring configuration class — beans, schedulers, or security rules are likely defined here.

---

### `AssetController.java` — *class*
- **Path:** `TrackWise-main/TrackWise-main/backend/src/main/java/org/godigit/trackwise/controller/AssetController.java`
- **Package:** `org.godigit.trackwise.controller`
- **Class annotations:** `RestController, RequestMapping("/api/assets"), RequiredArgsConstructor, PostMapping, GetMapping("/{id}"), GetMapping, PutMapping("/{id}"), DeleteMapping("/{id}"), PostMapping("/{assetId}/assign/{employeeId}"), PostMapping("/{assetId}/unassign"), GetMapping("/status/{status}"), GetMapping("/warranty-expiring"), RequestParam, RequestParam`
- **Detected role(s):** Controller / REST API

**Fields (approx.):** None detected or declared dynamically.

**Methods (approx.):**
- `createAsset(...)` — `public ResponseEntity<AssetResponse> createAsset(@Valid @RequestBody AssetRequest dto) {` Annotations: `PostMapping` — Mapping: `PostMapping` path: `/`
- `getAsset(...)` — `public ResponseEntity<AssetResponse> getAsset(@PathVariable UUID id) {` Annotations: `GetMapping("/{id}")` — Mapping: `GetMapping` path: `/{id}`
- `listAssets(...)` — `public ResponseEntity<Page<AssetResponse>> listAssets(Pageable pageable) {` Annotations: `GetMapping` — Mapping: `GetMapping` path: `/`
- `updateAsset(...)` — `public ResponseEntity<AssetResponse> updateAsset(@PathVariable UUID id, @RequestBody AssetRequest dto) {` Annotations: `PutMapping("/{id}")` — Mapping: `PutMapping` path: `/{id}`
- `deleteAsset(...)` — `public ResponseEntity<Void> deleteAsset(@PathVariable UUID id) {` Annotations: `DeleteMapping("/{id}")` — Mapping: `DeleteMapping` path: `/{id}`
- `assignToEmployee(...)` — `public ResponseEntity<AssetResponse> assignToEmployee(@PathVariable UUID assetId, @PathVariable UUID employeeId) {` Annotations: `PostMapping("/{assetId}/assign/{employeeId}")` — Mapping: `PostMapping` path: `/{assetId}/assign/{employeeId}`
- `unassignAsset(...)` — `public ResponseEntity<AssetResponse> unassignAsset(@PathVariable UUID assetId) {` Annotations: `PostMapping("/{assetId}/unassign")` — Mapping: `PostMapping` path: `/{assetId}/unassign`
- `findByStatus(...)` — `public ResponseEntity<List<AssetResponse>> findByStatus(@PathVariable AssetStatus status) {` Annotations: `GetMapping("/status/{status}")` — Mapping: `GetMapping` path: `/status/{status}`

**Purpose (in plain words):**
- This class looks like a REST controller exposing HTTP endpoints for `Asset` related operations. Look for methods annotated with `@GetMapping`, `@PostMapping`, etc. It likely autowires a corresponding Service class to handle business logic.

---

### `CheckInOutController.java` — *class*
- **Path:** `TrackWise-main/TrackWise-main/backend/src/main/java/org/godigit/trackwise/controller/CheckInOutController.java`
- **Package:** `org.godigit.trackwise.controller`
- **Class annotations:** `RestController, RequestMapping("/api/checkinout"), RequiredArgsConstructor, PostMapping("/checkout"), PostMapping("/checkin"), GetMapping("/asset/{assetId}/history"), GetMapping("/employee/{employeeId}/history"), PostMapping("/scan")`
- **Detected role(s):** Controller / REST API

**Fields (approx.):** None detected or declared dynamically.

**Methods (approx.):**
- `checkoutAsset(...)` — `public ResponseEntity<CheckInOutResponseDTO> checkoutAsset(@RequestBody CheckInOutRequestDTO request) {` Annotations: `PostMapping("/checkout")` — Mapping: `PostMapping` path: `/checkout`
- `checkinAsset(...)` — `public ResponseEntity<CheckInOutResponseDTO> checkinAsset(@RequestBody CheckInOutRequestDTO request) {` Annotations: `PostMapping("/checkin")` — Mapping: `PostMapping` path: `/checkin`
- `historyByAsset(...)` — `public ResponseEntity<List<CheckInOutResponseDTO>> historyByAsset(@PathVariable UUID assetId) {` Annotations: `GetMapping("/asset/{assetId}/history")` — Mapping: `GetMapping` path: `/asset/{assetId}/history`
- `historyByEmployee(...)` — `public ResponseEntity<List<CheckInOutResponseDTO>> historyByEmployee(@PathVariable UUID employeeId) {` Annotations: `GetMapping("/employee/{employeeId}/history")` — Mapping: `GetMapping` path: `/employee/{employeeId}/history`
- `processScan(...)` — `public ResponseEntity<CheckInOutResponseDTO> processScan(@RequestBody AssetScanRequestDTO request) {` Annotations: `PostMapping("/scan")` — Mapping: `PostMapping` path: `/scan`

**Purpose (in plain words):**
- This class looks like a REST controller exposing HTTP endpoints for `CheckInOut` related operations. Look for methods annotated with `@GetMapping`, `@PostMapping`, etc. It likely autowires a corresponding Service class to handle business logic.

---

### `EmployeeController.java` — *class*
- **Path:** `TrackWise-main/TrackWise-main/backend/src/main/java/org/godigit/trackwise/controller/EmployeeController.java`
- **Package:** `org.godigit.trackwise.controller`
- **Class annotations:** `RestController, RequestMapping("/api/employees"), RequiredArgsConstructor, PostMapping, GetMapping("/{id}"), GetMapping, PutMapping("/{id}"), RequestBody, DeleteMapping("/{id}"), GetMapping("/search")`
- **Detected role(s):** Controller / REST API

**Fields (approx.):** None detected or declared dynamically.

**Methods (approx.):**
- `createEmployee(...)` — `public ResponseEntity<EmployeeResponseDTO> createEmployee(@RequestBody EmployeeRequestDTO requestDTO) {` Annotations: `PostMapping` — Mapping: `PostMapping` path: `/`
- `getEmployee(...)` — `public ResponseEntity<EmployeeResponseDTO> getEmployee(@PathVariable UUID id) {` Annotations: `GetMapping("/{id}")` — Mapping: `GetMapping` path: `/{id}`
- `listEmployees(...)` — `public ResponseEntity<Page<EmployeeResponseDTO>> listEmployees(Pageable pageable) {` Annotations: `GetMapping` — Mapping: `GetMapping` path: `/`
- `updateEmployee(...)` — `public ResponseEntity<EmployeeResponseDTO> updateEmployee(@PathVariable UUID id,                                                               @RequestBody EmployeeRequestDTO requestDTO) {` Annotations: `PutMapping("/{id}")` — Mapping: `PutMapping` path: `/{id}`
- `deleteEmployee(...)` — `public ResponseEntity<Void> deleteEmployee(@PathVariable UUID id) {` Annotations: `DeleteMapping("/{id}")` — Mapping: `DeleteMapping` path: `/{id}`
- `findByEmail(...)` — `public ResponseEntity<EmployeeResponseDTO> findByEmail(@RequestParam String email) {` Annotations: `GetMapping("/search")` — Mapping: `GetMapping` path: `/search`

**Purpose (in plain words):**
- This class looks like a REST controller exposing HTTP endpoints for `Employee` related operations. Look for methods annotated with `@GetMapping`, `@PostMapping`, etc. It likely autowires a corresponding Service class to handle business logic.

---

### `IoTController.java` — *class*
- **Path:** `TrackWise-main/TrackWise-main/backend/src/main/java/org/godigit/trackwise/controller/IoTController.java`
- **Package:** `org.godigit.trackwise.controller`
- **Class annotations:** `RestController, RequestMapping("/api/iot"), RequiredArgsConstructor, PostMapping("/ingest"), PostMapping("/process/{assetId}"), PathVariable, RequestParam, RequestParam, RequestParam, RequestParam, RequestParam, PostMapping("/simulator/start"), PostMapping("/simulator/stop")`
- **Detected role(s):** Controller / REST API

**Fields (approx.):** None detected or declared dynamically.

**Methods (approx.):**
- `ingestData(...)` — `public ResponseEntity<IoTDataResponseDTO> ingestData(@RequestBody IoTDataRequestDTO request) {` Annotations: `PostMapping("/ingest")` — Mapping: `PostMapping` path: `/ingest`
- `processSensorData(...)` — `public ResponseEntity<IoTDataResponseDTO> processSensorData(             @PathVariable UUID assetId,             @RequestParam Double temperature,             @RequestParam Double batteryLevel,             @RequestParam Boolean inUse,             // Add the new location parameters             @RequestParam Double latitude,             @RequestParam Double longitude) {` Annotations: `PostMapping("/process/{assetId}")` — Mapping: `PostMapping` path: `/process/{assetId}`
- `startSimulator(...)` — `public ResponseEntity<Void> startSimulator() {` Annotations: `PostMapping("/simulator/start")` — Mapping: `PostMapping` path: `/simulator/start`
- `stopSimulator(...)` — `public ResponseEntity<Void> stopSimulator() {` Annotations: `PostMapping("/simulator/stop")` — Mapping: `PostMapping` path: `/simulator/stop`

**Purpose (in plain words):**
- This class looks like a REST controller exposing HTTP endpoints for `IoT` related operations. Look for methods annotated with `@GetMapping`, `@PostMapping`, etc. It likely autowires a corresponding Service class to handle business logic.

---

### `MaintenanceController.java` — *class*
- **Path:** `TrackWise-main/TrackWise-main/backend/src/main/java/org/godigit/trackwise/controller/MaintenanceController.java`
- **Package:** `org.godigit.trackwise.controller`
- **Class annotations:** `RestController, RequestMapping("/api/maintenance"), RequiredArgsConstructor, PostMapping("/{assetId}"), PathVariable, RequestBody, GetMapping("/{assetId}")`
- **Detected role(s):** Controller / REST API

**Fields (approx.):** None detected or declared dynamically.

**Methods (approx.):**
- `addMaintenance(...)` — `public ResponseEntity<MaintenanceResponseDTO> addMaintenance(             @PathVariable UUID assetId,             @RequestBody MaintenanceRequestDTO request) {` Annotations: `PostMapping("/{assetId}")` — Mapping: `PostMapping` path: `/{assetId}`
- `listByAsset(...)` — `public ResponseEntity<List<MaintenanceResponseDTO>> listByAsset(@PathVariable UUID assetId) {` Annotations: `GetMapping("/{assetId}")` — Mapping: `GetMapping` path: `/{assetId}`

**Purpose (in plain words):**
- This class looks like a REST controller exposing HTTP endpoints for `Maintenance` related operations. Look for methods annotated with `@GetMapping`, `@PostMapping`, etc. It likely autowires a corresponding Service class to handle business logic.

---

### `NotificationController.java` — *class*
- **Path:** `TrackWise-main/TrackWise-main/backend/src/main/java/org/godigit/trackwise/controller/NotificationController.java`
- **Package:** `org.godigit.trackwise.controller`
- **Class annotations:** `RestController, RequestMapping("/api/notifications"), RequiredArgsConstructor, PostMapping("/in-app"), RequestBody, PostMapping("/email")`
- **Detected role(s):** Controller / REST API

**Fields (approx.):** None detected or declared dynamically.

**Methods (approx.):**
- `createInAppNotification(...)` — `public ResponseEntity<NotificationResponseDTO> createInAppNotification(             @RequestBody NotificationRequestDTO request) {` Annotations: `PostMapping("/in-app")` — Mapping: `PostMapping` path: `/in-app`
- `sendEmail(...)` — `public ResponseEntity<Void> sendEmail(@RequestBody EmailRequestDTO request) {` Annotations: `PostMapping("/email")` — Mapping: `PostMapping` path: `/email`

**Purpose (in plain words):**
- This class looks like a REST controller exposing HTTP endpoints for `Notification` related operations. Look for methods annotated with `@GetMapping`, `@PostMapping`, etc. It likely autowires a corresponding Service class to handle business logic.

---

### `ReportController.java` — *class*
- **Path:** `TrackWise-main/TrackWise-main/backend/src/main/java/org/godigit/trackwise/controller/ReportController.java`
- **Package:** `org.godigit.trackwise.controller`
- **Class annotations:** `RestController, RequestMapping("/api/reports"), RequiredArgsConstructor, GetMapping("/warranty-expiry"), RequestParam("from"), RequestParam("to"), GetMapping("/asset-aging"), RequestParam("olderThanDays")`
- **Detected role(s):** Controller / REST API

**Fields (approx.):** None detected or declared dynamically.

**Methods (approx.):** None detected.

**Purpose (in plain words):**
- This class looks like a REST controller exposing HTTP endpoints for `Report` related operations. Look for methods annotated with `@GetMapping`, `@PostMapping`, etc. It likely autowires a corresponding Service class to handle business logic.

---

### `WarrantyController.java` — *class*
- **Path:** `TrackWise-main/TrackWise-main/backend/src/main/java/org/godigit/trackwise/controller/WarrantyController.java`
- **Package:** `org.godigit.trackwise.controller`
- **Class annotations:** `RestController, RequestMapping("/api/warranties"), RequiredArgsConstructor, PostMapping, GetMapping("/expiring"), RequestParam, RequestParam, PutMapping("/{id}/extend"), PathVariable("id"), RequestParam`
- **Detected role(s):** Controller / REST API

**Fields (approx.):** None detected or declared dynamically.

**Methods (approx.):**
- `createOrUpdate(...)` — `public ResponseEntity<WarrantyResponseDTO> createOrUpdate(@RequestBody WarrantyRequestDTO request) {` Annotations: `PostMapping` — Mapping: `PostMapping` path: `/`

**Purpose (in plain words):**
- This class looks like a REST controller exposing HTTP endpoints for `Warranty` related operations. Look for methods annotated with `@GetMapping`, `@PostMapping`, etc. It likely autowires a corresponding Service class to handle business logic.

---

### `AssetRequest.java` — *class*
- **Path:** `TrackWise-main/TrackWise-main/backend/src/main/java/org/godigit/trackwise/dto/AssetRequest.java`
- **Package:** `org.godigit.trackwise.dto`
- **Class annotations:** `Getter, Setter`

**Fields (approx.):**
- `name` : `String` (private)
- `categoryId` : `UUID` (private)
- `status` : `String` (private)
- `warrantyExpiryDate` : `LocalDate` (private)
- `employeeId` : `UUID` (private)
- `purchaseDate` : `LocalDate` (private)
- `serialNumber` : `String` (private)

**Methods (approx.):** None detected.

**Purpose (in plain words):**
- General-purpose class/DTO/utility — open the file to see exact responsibilities.

---

### `AssetResponse.java` — *class*
- **Path:** `TrackWise-main/TrackWise-main/backend/src/main/java/org/godigit/trackwise/dto/AssetResponse.java`
- **Package:** `org.godigit.trackwise.dto`
- **Class annotations:** `Getter, Setter`

**Fields (approx.):**
- `id` : `UUID` (private)
- `name` : `String` (private)
- `categoryName` : `String` (private)
- `status` : `String` (private)
- `assignedEmployee` : `String` (private)
- `purchaseDate` : `LocalDate` (private)
- `serialNumber` : `String` (private)
- `warrantyExpiryDate` : `LocalDate` (private)

**Methods (approx.):** None detected.

**Purpose (in plain words):**
- General-purpose class/DTO/utility — open the file to see exact responsibilities.

---

### `AssetScanRequestDTO.java` — *class*
- **Path:** `TrackWise-main/TrackWise-main/backend/src/main/java/org/godigit/trackwise/dto/AssetScanRequestDTO.java`
- **Package:** `org.godigit.trackwise.dto`
- **Class annotations:** `Data`

**Fields (approx.):**
- `assetId` : `UUID` (private)
- `employeeId` : `UUID` (private)

**Methods (approx.):** None detected.

**Purpose (in plain words):**
- General-purpose class/DTO/utility — open the file to see exact responsibilities.

---

### `CheckInOutRequestDTO.java` — *class*
- **Path:** `TrackWise-main/TrackWise-main/backend/src/main/java/org/godigit/trackwise/dto/CheckInOutRequestDTO.java`
- **Package:** `org.godigit.trackwise.dto`
- **Class annotations:** `Data`

**Fields (approx.):**
- `assetId` : `UUID` (private)
- `employeeId` : `UUID` (private)

**Methods (approx.):** None detected.

**Purpose (in plain words):**
- General-purpose class/DTO/utility — open the file to see exact responsibilities.

---

### `CheckInOutResponseDTO.java` — *class*
- **Path:** `TrackWise-main/TrackWise-main/backend/src/main/java/org/godigit/trackwise/dto/CheckInOutResponseDTO.java`
- **Package:** `org.godigit.trackwise.dto`
- **Class annotations:** `Data`

**Fields (approx.):**
- `id` : `UUID` (private)
- `assetId` : `UUID` (private)
- `assetName` : `String` (private)
- `employeeId` : `UUID` (private)
- `employeeName` : `String` (private)
- `checkOutTime` : `Instant` (private)
- `checkInTime` : `Instant` (private)

**Methods (approx.):** None detected.

**Purpose (in plain words):**
- General-purpose class/DTO/utility — open the file to see exact responsibilities.

---

### `EmailRequestDTO.java` — *class*
- **Path:** `TrackWise-main/TrackWise-main/backend/src/main/java/org/godigit/trackwise/dto/EmailRequestDTO.java`
- **Package:** `org.godigit.trackwise.dto`
- **Class annotations:** `Data`

**Fields (approx.):**
- `to` : `String` (private)
- `subject` : `String` (private)
- `body` : `String` (private)

**Methods (approx.):** None detected.

**Purpose (in plain words):**
- General-purpose class/DTO/utility — open the file to see exact responsibilities.

---

### `EmployeeRequestDTO.java` — *class*
- **Path:** `TrackWise-main/TrackWise-main/backend/src/main/java/org/godigit/trackwise/dto/EmployeeRequestDTO.java`
- **Package:** `org.godigit.trackwise.dto`
- **Class annotations:** `Data`

**Fields (approx.):**
- `firstName` : `String` (private)
- `lastName` : `String` (private)
- `email` : `String` (private)
- `phone` : `String` (private)
- `departmentId` : `UUID` (private)

**Methods (approx.):** None detected.

**Purpose (in plain words):**
- General-purpose class/DTO/utility — open the file to see exact responsibilities.

---

### `EmployeeResponseDTO.java` — *class*
- **Path:** `TrackWise-main/TrackWise-main/backend/src/main/java/org/godigit/trackwise/dto/EmployeeResponseDTO.java`
- **Package:** `org.godigit.trackwise.dto`
- **Class annotations:** `Data`

**Fields (approx.):**
- `id` : `UUID` (private)
- `firstName` : `String` (private)
- `lastName` : `String` (private)
- `email` : `String` (private)
- `phone` : `String` (private)
- `departmentId` : `UUID` (private)
- `departmentName` : `String` (private)

**Methods (approx.):** None detected.

**Purpose (in plain words):**
- General-purpose class/DTO/utility — open the file to see exact responsibilities.

---

### `IoTDataRequestDTO.java` — *class*
- **Path:** `TrackWise-main/TrackWise-main/backend/src/main/java/org/godigit/trackwise/dto/IoTDataRequestDTO.java`
- **Package:** `org.godigit.trackwise.dto`
- **Class annotations:** `Data`

**Fields (approx.):**
- `assetId` : `UUID` (private)
- `temperature` : `Double` (private)
- `batteryLevel` : `Double` (private)
- `inUse` : `Boolean` (private)
- `latitude` : `Double` (private)
- `longitude` : `Double` (private)

**Methods (approx.):** None detected.

**Purpose (in plain words):**
- General-purpose class/DTO/utility — open the file to see exact responsibilities.

---

### `IoTDataResponseDTO.java` — *class*
- **Path:** `TrackWise-main/TrackWise-main/backend/src/main/java/org/godigit/trackwise/dto/IoTDataResponseDTO.java`
- **Package:** `org.godigit.trackwise.dto`
- **Class annotations:** `Data`

**Fields (approx.):**
- `logId` : `UUID` (private)
- `assetId` : `UUID` (private)
- `assetName` : `String` (private)
- `temperature` : `Double` (private)
- `batteryLevel` : `Double` (private)
- `inUse` : `Boolean` (private)
- `timestamp` : `Instant` (private)

**Methods (approx.):** None detected.

**Purpose (in plain words):**
- General-purpose class/DTO/utility — open the file to see exact responsibilities.

---

### `MaintenanceRequestDTO.java` — *class*
- **Path:** `TrackWise-main/TrackWise-main/backend/src/main/java/org/godigit/trackwise/dto/MaintenanceRequestDTO.java`
- **Package:** `org.godigit.trackwise.dto`
- **Class annotations:** `Data`

**Fields (approx.):**
- `description` : `String` (private)
- `maintenanceDate` : `LocalDate` (private)
- `performedBy` : `String` (private)

**Methods (approx.):** None detected.

**Purpose (in plain words):**
- General-purpose class/DTO/utility — open the file to see exact responsibilities.

---

### `MaintenanceResponseDTO.java` — *class*
- **Path:** `TrackWise-main/TrackWise-main/backend/src/main/java/org/godigit/trackwise/dto/MaintenanceResponseDTO.java`
- **Package:** `org.godigit.trackwise.dto`
- **Class annotations:** `Data`

**Fields (approx.):**
- `logId` : `UUID` (private)
- `assetId` : `UUID` (private)
- `assetName` : `String` (private)
- `description` : `String` (private)
- `maintenanceDate` : `LocalDate` (private)
- `performedBy` : `String` (private)

**Methods (approx.):** None detected.

**Purpose (in plain words):**
- General-purpose class/DTO/utility — open the file to see exact responsibilities.

---

### `NotificationRequestDTO.java` — *class*
- **Path:** `TrackWise-main/TrackWise-main/backend/src/main/java/org/godigit/trackwise/dto/NotificationRequestDTO.java`
- **Package:** `org.godigit.trackwise.dto`
- **Class annotations:** `Data`

**Fields (approx.):**
- `recipientId` : `UUID` (private)
- `message` : `String` (private)

**Methods (approx.):** None detected.

**Purpose (in plain words):**
- General-purpose class/DTO/utility — open the file to see exact responsibilities.

---

### `NotificationResponseDTO.java` — *class*
- **Path:** `TrackWise-main/TrackWise-main/backend/src/main/java/org/godigit/trackwise/dto/NotificationResponseDTO.java`
- **Package:** `org.godigit.trackwise.dto`
- **Class annotations:** `Data`

**Fields (approx.):**
- `id` : `UUID` (private)
- `recipientId` : `UUID` (private)
- `recipientName` : `String` (private)
- `message` : `String` (private)
- `read` : `boolean` (private)
- `createdAt` : `Instant` (private)

**Methods (approx.):** None detected.

**Purpose (in plain words):**
- General-purpose class/DTO/utility — open the file to see exact responsibilities.

---

### `WarrantyRequestDTO.java` — *class*
- **Path:** `TrackWise-main/TrackWise-main/backend/src/main/java/org/godigit/trackwise/dto/WarrantyRequestDTO.java`
- **Package:** `org.godigit.trackwise.dto`
- **Class annotations:** `Data`

**Fields (approx.):**
- `assetId` : `UUID` (private)
- `startDate` : `LocalDate` (private)
- `endDate` : `LocalDate` (private)
- `vendor` : `String` (private)

**Methods (approx.):** None detected.

**Purpose (in plain words):**
- General-purpose class/DTO/utility — open the file to see exact responsibilities.

---

### `WarrantyResponseDTO.java` — *class*
- **Path:** `TrackWise-main/TrackWise-main/backend/src/main/java/org/godigit/trackwise/dto/WarrantyResponseDTO.java`
- **Package:** `org.godigit.trackwise.dto`
- **Class annotations:** `Data`

**Fields (approx.):**
- `warrantyId` : `UUID` (private)
- `assetId` : `UUID` (private)
- `assetName` : `String` (private)
- `startDate` : `LocalDate` (private)
- `endDate` : `LocalDate` (private)
- `vendor` : `String` (private)

**Methods (approx.):** None detected.

**Purpose (in plain words):**
- General-purpose class/DTO/utility — open the file to see exact responsibilities.

---

### `NotFoundException.java` — *class*
- **Path:** `TrackWise-main/TrackWise-main/backend/src/main/java/org/godigit/trackwise/exception/NotFoundException.java`
- **Package:** `org.godigit.trackwise.exception`
- **Extends:** `RuntimeException`

**Fields (approx.):** None detected or declared dynamically.

**Methods (approx.):**
- `public NotFoundException(...)` — `public NotFoundException(String message) {` 

**Purpose (in plain words):**
- General-purpose class/DTO/utility — open the file to see exact responsibilities.

---

### `AssetMapper.java` — *class*
- **Path:** `TrackWise-main/TrackWise-main/backend/src/main/java/org/godigit/trackwise/mapper/AssetMapper.java`
- **Package:** `org.godigit.trackwise.mapper`
- **Class annotations:** `Component`

**Fields (approx.):** None detected or declared dynamically.

**Methods (approx.):**
- `toEntity(...)` — `public Asset toEntity(AssetRequest request, AssetCategory category, Employee employee) {` 
- `updateEntity(...)` — `public void updateEntity(Asset asset, AssetRequest request, AssetCategory category, Employee employee) {` 
- `toResponse(...)` — `public AssetResponse toResponse(Asset asset) {` 

**Purpose (in plain words):**
- General-purpose class/DTO/utility — open the file to see exact responsibilities.

---

### `CheckInOutMapper.java` — *class*
- **Path:** `TrackWise-main/TrackWise-main/backend/src/main/java/org/godigit/trackwise/mapper/CheckInOutMapper.java`
- **Package:** `org.godigit.trackwise.mapper`

**Fields (approx.):** None detected or declared dynamically.

**Methods (approx.):**
- `toDTO(...)` — `public static CheckInOutResponseDTO toDTO(CheckInOutLog log) {` 

**Purpose (in plain words):**
- General-purpose class/DTO/utility — open the file to see exact responsibilities.

---

### `EmployeeMapper.java` — *class*
- **Path:** `TrackWise-main/TrackWise-main/backend/src/main/java/org/godigit/trackwise/mapper/EmployeeMapper.java`
- **Package:** `org.godigit.trackwise.mapper`

**Fields (approx.):** None detected or declared dynamically.

**Methods (approx.):**
- `toEntity(...)` — `public static Employee toEntity(EmployeeRequestDTO dto, Department department) {` 
- `toDto(...)` — `public static EmployeeResponseDTO toDto(Employee employee) {` 

**Purpose (in plain words):**
- General-purpose class/DTO/utility — open the file to see exact responsibilities.

---

### `IoTDataMapper.java` — *class*
- **Path:** `TrackWise-main/TrackWise-main/backend/src/main/java/org/godigit/trackwise/mapper/IoTDataMapper.java`
- **Package:** `org.godigit.trackwise.mapper`

**Fields (approx.):** None detected or declared dynamically.

**Methods (approx.):**
- `toResponseDTO(...)` — `public static IoTDataResponseDTO toResponseDTO(IoTData data) {` 

**Purpose (in plain words):**
- General-purpose class/DTO/utility — open the file to see exact responsibilities.

---

### `MaintenanceMapper.java` — *class*
- **Path:** `TrackWise-main/TrackWise-main/backend/src/main/java/org/godigit/trackwise/mapper/MaintenanceMapper.java`
- **Package:** `org.godigit.trackwise.mapper`

**Fields (approx.):** None detected or declared dynamically.

**Methods (approx.):**
- `toResponseDTO(...)` — `public static MaintenanceResponseDTO toResponseDTO(MaintenanceLog log) {` 

**Purpose (in plain words):**
- General-purpose class/DTO/utility — open the file to see exact responsibilities.

---

### `NotificationMapper.java` — *class*
- **Path:** `TrackWise-main/TrackWise-main/backend/src/main/java/org/godigit/trackwise/mapper/NotificationMapper.java`
- **Package:** `org.godigit.trackwise.mapper`

**Fields (approx.):** None detected or declared dynamically.

**Methods (approx.):**
- `toResponseDTO(...)` — `public static NotificationResponseDTO toResponseDTO(Notification notification) {` 

**Purpose (in plain words):**
- General-purpose class/DTO/utility — open the file to see exact responsibilities.

---

### `WarrantyMapper.java` — *class*
- **Path:** `TrackWise-main/TrackWise-main/backend/src/main/java/org/godigit/trackwise/mapper/WarrantyMapper.java`
- **Package:** `org.godigit.trackwise.mapper`

**Fields (approx.):** None detected or declared dynamically.

**Methods (approx.):**
- `toResponseDTO(...)` — `public static WarrantyResponseDTO toResponseDTO(Warranty warranty) {` 

**Purpose (in plain words):**
- General-purpose class/DTO/utility — open the file to see exact responsibilities.

---

### `Asset.java` — *class*
- **Path:** `TrackWise-main/TrackWise-main/backend/src/main/java/org/godigit/trackwise/model/Asset.java`
- **Package:** `org.godigit.trackwise.model`
- **Class annotations:** `Getter, Setter, Entity, Table(name = "assets"), ManyToOne, JoinColumn(name = "category_id"), Enumerated(EnumType.STRING), Column(columnDefinition = "asset_status"), ManyToOne, JoinColumn(name = "employee_id"), OneToOne(mappedBy = "asset", cascade = CascadeType.ALL, orphanRemoval = true)`
- **Detected role(s):** JPA Entity
- **Extends:** `BaseEntity`
- **Detected JPA relationships/annotations in class:** `@ManyToOne, @OneToOne, @JoinColumn`

**Fields (approx.):**
- `name` : `String` (private)
- `category` : `AssetCategory` (private)
- `status` : `AssetStatus` (private)
- `warrantyExpiryDate` : `LocalDate` (private)
- `assignedTo` : `Employee` (private)
- `purchaseDate` : `LocalDate` (private)
- `serialNumber` : `String` (private)
- `warranty` : `Warranty` (private)

**Methods (approx.):** None detected.

**Purpose (in plain words):**
- This is a JPA entity mapping to a database table. Fields are columns; look for `@Id`, `@GeneratedValue`, and relationship annotations like `@ManyToOne` to see associations.

---

### `AssetCategory.java` — *class*
- **Path:** `TrackWise-main/TrackWise-main/backend/src/main/java/org/godigit/trackwise/model/AssetCategory.java`
- **Package:** `org.godigit.trackwise.model`
- **Class annotations:** `Getter, Setter, Entity, Table(name = "asset_categories")`
- **Detected role(s):** JPA Entity
- **Extends:** `BaseEntity`

**Fields (approx.):**
- `name` : `String` (private)
- `description` : `String` (private)

**Methods (approx.):** None detected.

**Purpose (in plain words):**
- This is a JPA entity mapping to a database table. Fields are columns; look for `@Id`, `@GeneratedValue`, and relationship annotations like `@ManyToOne` to see associations.

---

### `AssetStatus.java` — *enum*
- **Path:** `TrackWise-main/TrackWise-main/backend/src/main/java/org/godigit/trackwise/model/AssetStatus.java`
- **Package:** `org.godigit.trackwise.model`

**Fields (approx.):** None detected or declared dynamically.

**Methods (approx.):** None detected.

**Purpose (in plain words):**
- General-purpose class/DTO/utility — open the file to see exact responsibilities.

---

### `BaseEntity.java` — *class*
- **Path:** `TrackWise-main/TrackWise-main/backend/src/main/java/org/godigit/trackwise/model/BaseEntity.java`
- **Package:** `org.godigit.trackwise.model`
- **Class annotations:** `Getter, Setter, MappedSuperclass, Id, GeneratedValue, CreationTimestamp, Column(updatable = false), UpdateTimestamp`

**Fields (approx.):**
- `id` : `UUID` (private)
- `createdAt` : `Instant` (private)
- `updatedAt` : `Instant` (private)

**Methods (approx.):** None detected.

**Purpose (in plain words):**
- General-purpose class/DTO/utility — open the file to see exact responsibilities.

---

### `CheckInOutAction.java` — *enum*
- **Path:** `TrackWise-main/TrackWise-main/backend/src/main/java/org/godigit/trackwise/model/CheckInOutAction.java`
- **Package:** `org.godigit.trackwise.model`

**Fields (approx.):** None detected or declared dynamically.

**Methods (approx.):** None detected.

**Purpose (in plain words):**
- General-purpose class/DTO/utility — open the file to see exact responsibilities.

---

### `CheckInOutLog.java` — *class*
- **Path:** `TrackWise-main/TrackWise-main/backend/src/main/java/org/godigit/trackwise/model/CheckInOutLog.java`
- **Package:** `org.godigit.trackwise.model`
- **Class annotations:** `Getter, Setter, Entity, Table(name = "check_in_out_logs"), ManyToOne, JoinColumn(name = "asset_id"), ManyToOne, JoinColumn(name = "employee_id"), Enumerated(EnumType.STRING), Column(nullable = false), Column(nullable = false)`
- **Detected role(s):** JPA Entity
- **Extends:** `BaseEntity`
- **Detected JPA relationships/annotations in class:** `@ManyToOne, @JoinColumn`

**Fields (approx.):**
- `asset` : `Asset` (private)
- `employee` : `Employee` (private)
- `action` : `CheckInOutAction` (private)
- `checkOutTime` : `Instant` (private)
- `checkInTime` : `Instant` (private)

**Methods (approx.):** None detected.

**Purpose (in plain words):**
- This is a JPA entity mapping to a database table. Fields are columns; look for `@Id`, `@GeneratedValue`, and relationship annotations like `@ManyToOne` to see associations.

---

### `Department.java` — *class*
- **Path:** `TrackWise-main/TrackWise-main/backend/src/main/java/org/godigit/trackwise/model/Department.java`
- **Package:** `org.godigit.trackwise.model`
- **Class annotations:** `Getter, Setter, Entity, Table(name = "departments")`
- **Detected role(s):** JPA Entity
- **Extends:** `BaseEntity`

**Fields (approx.):**
- `name` : `String` (private)
- `location` : `String` (private)

**Methods (approx.):** None detected.

**Purpose (in plain words):**
- This is a JPA entity mapping to a database table. Fields are columns; look for `@Id`, `@GeneratedValue`, and relationship annotations like `@ManyToOne` to see associations.

---

### `Employee.java` — *class*
- **Path:** `TrackWise-main/TrackWise-main/backend/src/main/java/org/godigit/trackwise/model/Employee.java`
- **Package:** `org.godigit.trackwise.model`
- **Class annotations:** `Getter, Setter, Entity, Table(name = "employees"), ManyToOne, JoinColumn(name = "department_id")`
- **Detected role(s):** JPA Entity
- **Extends:** `BaseEntity`
- **Detected JPA relationships/annotations in class:** `@ManyToOne, @JoinColumn`

**Fields (approx.):**
- `firstName` : `String` (private)
- `lastName` : `String` (private)
- `email` : `String` (private)
- `phone` : `String` (private)
- `department` : `Department` (private)

**Methods (approx.):** None detected.

**Purpose (in plain words):**
- This is a JPA entity mapping to a database table. Fields are columns; look for `@Id`, `@GeneratedValue`, and relationship annotations like `@ManyToOne` to see associations.

---

### `IoTData.java` — *class*
- **Path:** `TrackWise-main/TrackWise-main/backend/src/main/java/org/godigit/trackwise/model/IoTData.java`
- **Package:** `org.godigit.trackwise.model`
- **Class annotations:** `Getter, Setter, Entity, Table(name = "iot_data"), ManyToOne, JoinColumn(name = "asset_id"), Column(nullable = false)`
- **Detected role(s):** JPA Entity
- **Extends:** `BaseEntity`
- **Detected JPA relationships/annotations in class:** `@ManyToOne, @JoinColumn`

**Fields (approx.):**
- `asset` : `Asset` (private)
- `temperature` : `Double` (private)
- `batteryLevel` : `Double` (private)
- `inUse` : `Boolean` (private)
- `timestamp` : `Instant` (private)
- `latitude` : `Double` (private)
- `longitude` : `Double` (private)

**Methods (approx.):** None detected.

**Purpose (in plain words):**
- This is a JPA entity mapping to a database table. Fields are columns; look for `@Id`, `@GeneratedValue`, and relationship annotations like `@ManyToOne` to see associations.

---

### `MaintenanceLog.java` — *class*
- **Path:** `TrackWise-main/TrackWise-main/backend/src/main/java/org/godigit/trackwise/model/MaintenanceLog.java`
- **Package:** `org.godigit.trackwise.model`
- **Class annotations:** `Getter, Setter, Entity, Table(name = "maintenance_logs"), ManyToOne, JoinColumn(name = "asset_id")`
- **Detected role(s):** JPA Entity
- **Extends:** `BaseEntity`
- **Detected JPA relationships/annotations in class:** `@ManyToOne, @JoinColumn`

**Fields (approx.):**
- `asset` : `Asset` (private)
- `description` : `String` (private)
- `maintenanceDate` : `LocalDate` (private)
- `performedBy` : `String` (private)

**Methods (approx.):** None detected.

**Purpose (in plain words):**
- This is a JPA entity mapping to a database table. Fields are columns; look for `@Id`, `@GeneratedValue`, and relationship annotations like `@ManyToOne` to see associations.

---

### `Notification.java` — *class*
- **Path:** `TrackWise-main/TrackWise-main/backend/src/main/java/org/godigit/trackwise/model/Notification.java`
- **Package:** `org.godigit.trackwise.model`
- **Class annotations:** `Entity, Table(name = "notifications"), Getter, Setter, Builder, NoArgsConstructor, AllArgsConstructor, Id, GeneratedValue, ManyToOne(fetch = FetchType.LAZY), JoinColumn(name = "recipient_id", nullable = false), Column(nullable = false)`
- **Detected role(s):** JPA Entity
- **Detected JPA relationships/annotations in class:** `@ManyToOne, @JoinColumn`

**Fields (approx.):**
- `id` : `UUID` (private)
- `recipient` : `Employee` (private)
- `message` : `String` (private)
- `read` : `boolean` (private)
- `createdAt` : `Instant` (private)

**Methods (approx.):** None detected.

**Purpose (in plain words):**
- This is a JPA entity mapping to a database table. Fields are columns; look for `@Id`, `@GeneratedValue`, and relationship annotations like `@ManyToOne` to see associations.

---

### `NotificationType.java` — *enum*
- **Path:** `TrackWise-main/TrackWise-main/backend/src/main/java/org/godigit/trackwise/model/NotificationType.java`
- **Package:** `org.godigit.trackwise.model`

**Fields (approx.):** None detected or declared dynamically.

**Methods (approx.):** None detected.

**Purpose (in plain words):**
- General-purpose class/DTO/utility — open the file to see exact responsibilities.

---

### `Warranty.java` — *class*
- **Path:** `TrackWise-main/TrackWise-main/backend/src/main/java/org/godigit/trackwise/model/Warranty.java`
- **Package:** `org.godigit.trackwise.model`
- **Class annotations:** `Getter, Setter, Entity, Table(name = "warranties"), OneToOne, JoinColumn(name = "asset_id", unique = true)`
- **Detected role(s):** JPA Entity
- **Extends:** `BaseEntity`
- **Detected JPA relationships/annotations in class:** `@OneToOne, @JoinColumn`

**Fields (approx.):**
- `asset` : `Asset` (private)
- `startDate` : `LocalDate` (private)
- `endDate` : `LocalDate` (private)
- `vendor` : `String` (private)

**Methods (approx.):** None detected.

**Purpose (in plain words):**
- This is a JPA entity mapping to a database table. Fields are columns; look for `@Id`, `@GeneratedValue`, and relationship annotations like `@ManyToOne` to see associations.

---

### `AssetCategoryRepository.java` — *interface*
- **Path:** `TrackWise-main/TrackWise-main/backend/src/main/java/org/godigit/trackwise/repository/AssetCategoryRepository.java`
- **Package:** `org.godigit.trackwise.repository`
- **Detected role(s):** Repository
- **Extends:** `JpaRepository<AssetCategory, UUID>`
- **JpaRepository Entity:** `AssetCategory` (ID type: `UUID`)

**Fields (approx.):** None detected or declared dynamically.

**Methods (approx.):** None detected.

**Purpose (in plain words):**
- This interface/class provides data access for an entity, typically by extending `JpaRepository` or `CrudRepository`. Methods may include query methods (findBy..., existsBy...).

---

### `AssetRepository.java` — *interface*
- **Path:** `TrackWise-main/TrackWise-main/backend/src/main/java/org/godigit/trackwise/repository/AssetRepository.java`
- **Package:** `org.godigit.trackwise.repository`
- **Class annotations:** `Query("SELECT a FROM Asset a WHERE a.purchaseDate < CURRENT_DATE - 1 YEAR"), Query("SELECT a FROM Asset a WHERE a.warrantyExpiryDate BETWEEN :from AND :to")`
- **Detected role(s):** Repository
- **Extends:** `JpaRepository<Asset, UUID>`
- **JpaRepository Entity:** `Asset` (ID type: `UUID`)

**Fields (approx.):** None detected or declared dynamically.

**Methods (approx.):** None detected.

**Purpose (in plain words):**
- This interface/class provides data access for an entity, typically by extending `JpaRepository` or `CrudRepository`. Methods may include query methods (findBy..., existsBy...).

---

### `CheckInOutLogRepository.java` — *interface*
- **Path:** `TrackWise-main/TrackWise-main/backend/src/main/java/org/godigit/trackwise/repository/CheckInOutLogRepository.java`
- **Package:** `org.godigit.trackwise.repository`
- **Detected role(s):** Repository
- **Extends:** `JpaRepository<CheckInOutLog, UUID>`
- **JpaRepository Entity:** `CheckInOutLog` (ID type: `UUID`)

**Fields (approx.):** None detected or declared dynamically.

**Methods (approx.):** None detected.

**Purpose (in plain words):**
- This interface/class provides data access for an entity, typically by extending `JpaRepository` or `CrudRepository`. Methods may include query methods (findBy..., existsBy...).

---

### `DepartmentRepository.java` — *interface*
- **Path:** `TrackWise-main/TrackWise-main/backend/src/main/java/org/godigit/trackwise/repository/DepartmentRepository.java`
- **Package:** `org.godigit.trackwise.repository`
- **Class annotations:** `Repository`
- **Detected role(s):** Repository
- **Extends:** `JpaRepository<Department, UUID>`
- **JpaRepository Entity:** `Department` (ID type: `UUID`)

**Fields (approx.):** None detected or declared dynamically.

**Methods (approx.):** None detected.

**Purpose (in plain words):**
- This interface/class provides data access for an entity, typically by extending `JpaRepository` or `CrudRepository`. Methods may include query methods (findBy..., existsBy...).

---

### `EmployeeRepository.java` — *interface*
- **Path:** `TrackWise-main/TrackWise-main/backend/src/main/java/org/godigit/trackwise/repository/EmployeeRepository.java`
- **Package:** `org.godigit.trackwise.repository`
- **Detected role(s):** Repository
- **Extends:** `JpaRepository<Employee, UUID>`
- **JpaRepository Entity:** `Employee` (ID type: `UUID`)

**Fields (approx.):** None detected or declared dynamically.

**Methods (approx.):** None detected.

**Purpose (in plain words):**
- This interface/class provides data access for an entity, typically by extending `JpaRepository` or `CrudRepository`. Methods may include query methods (findBy..., existsBy...).

---

### `IoTDataRepository.java` — *interface*
- **Path:** `TrackWise-main/TrackWise-main/backend/src/main/java/org/godigit/trackwise/repository/IoTDataRepository.java`
- **Package:** `org.godigit.trackwise.repository`
- **Class annotations:** `Repository`
- **Detected role(s):** Repository
- **Extends:** `JpaRepository<IoTData, UUID>`
- **JpaRepository Entity:** `IoTData` (ID type: `UUID`)

**Fields (approx.):** None detected or declared dynamically.

**Methods (approx.):** None detected.

**Purpose (in plain words):**
- This interface/class provides data access for an entity, typically by extending `JpaRepository` or `CrudRepository`. Methods may include query methods (findBy..., existsBy...).

---

### `MaintenanceLogRepository.java` — *interface*
- **Path:** `TrackWise-main/TrackWise-main/backend/src/main/java/org/godigit/trackwise/repository/MaintenanceLogRepository.java`
- **Package:** `org.godigit.trackwise.repository`
- **Detected role(s):** Repository
- **Extends:** `JpaRepository<MaintenanceLog, UUID>`
- **JpaRepository Entity:** `MaintenanceLog` (ID type: `UUID`)

**Fields (approx.):** None detected or declared dynamically.

**Methods (approx.):** None detected.

**Purpose (in plain words):**
- This interface/class provides data access for an entity, typically by extending `JpaRepository` or `CrudRepository`. Methods may include query methods (findBy..., existsBy...).

---

### `NotificationRepository.java` — *interface*
- **Path:** `TrackWise-main/TrackWise-main/backend/src/main/java/org/godigit/trackwise/repository/NotificationRepository.java`
- **Package:** `org.godigit.trackwise.repository`
- **Detected role(s):** Repository
- **Extends:** `JpaRepository<Notification, UUID>`
- **JpaRepository Entity:** `Notification` (ID type: `UUID`)

**Fields (approx.):** None detected or declared dynamically.

**Methods (approx.):** None detected.

**Purpose (in plain words):**
- This interface/class provides data access for an entity, typically by extending `JpaRepository` or `CrudRepository`. Methods may include query methods (findBy..., existsBy...).

---

### `WarrantyRepository.java` — *interface*
- **Path:** `TrackWise-main/TrackWise-main/backend/src/main/java/org/godigit/trackwise/repository/WarrantyRepository.java`
- **Package:** `org.godigit.trackwise.repository`
- **Detected role(s):** Repository
- **Extends:** `JpaRepository<Warranty, UUID>`
- **JpaRepository Entity:** `Warranty` (ID type: `UUID`)

**Fields (approx.):** None detected or declared dynamically.

**Methods (approx.):** None detected.

**Purpose (in plain words):**
- This interface/class provides data access for an entity, typically by extending `JpaRepository` or `CrudRepository`. Methods may include query methods (findBy..., existsBy...).

---

### `AssetService.java` — *interface*
- **Path:** `TrackWise-main/TrackWise-main/backend/src/main/java/org/godigit/trackwise/service/AssetService.java`
- **Package:** `org.godigit.trackwise.service`
- **Detected role(s):** Service / Business Logic

**Fields (approx.):** None detected or declared dynamically.

**Methods (approx.):** None detected.

**Purpose (in plain words):**
- This class contains business logic for domain `Asset`. It probably interacts with one or more Repository interfaces and performs validations, transforms (DTO -> Entity), and transactions.

---

### `CheckInOutService.java` — *interface*
- **Path:** `TrackWise-main/TrackWise-main/backend/src/main/java/org/godigit/trackwise/service/CheckInOutService.java`
- **Package:** `org.godigit.trackwise.service`
- **Detected role(s):** Service / Business Logic

**Fields (approx.):** None detected or declared dynamically.

**Methods (approx.):** None detected.

**Purpose (in plain words):**
- This class contains business logic for domain `CheckInOut`. It probably interacts with one or more Repository interfaces and performs validations, transforms (DTO -> Entity), and transactions.

---

### `EmployeeService.java` — *interface*
- **Path:** `TrackWise-main/TrackWise-main/backend/src/main/java/org/godigit/trackwise/service/EmployeeService.java`
- **Package:** `org.godigit.trackwise.service`
- **Detected role(s):** Service / Business Logic

**Fields (approx.):** None detected or declared dynamically.

**Methods (approx.):** None detected.

**Purpose (in plain words):**
- This class contains business logic for domain `Employee`. It probably interacts with one or more Repository interfaces and performs validations, transforms (DTO -> Entity), and transactions.

---

### `IoTService.java` — *interface*
- **Path:** `TrackWise-main/TrackWise-main/backend/src/main/java/org/godigit/trackwise/service/IoTService.java`
- **Package:** `org.godigit.trackwise.service`
- **Detected role(s):** Service / Business Logic

**Fields (approx.):** None detected or declared dynamically.

**Methods (approx.):** None detected.

**Purpose (in plain words):**
- This class contains business logic for domain `IoT`. It probably interacts with one or more Repository interfaces and performs validations, transforms (DTO -> Entity), and transactions.

---

### `MaintenanceService.java` — *interface*
- **Path:** `TrackWise-main/TrackWise-main/backend/src/main/java/org/godigit/trackwise/service/MaintenanceService.java`
- **Package:** `org.godigit.trackwise.service`
- **Detected role(s):** Service / Business Logic

**Fields (approx.):** None detected or declared dynamically.

**Methods (approx.):** None detected.

**Purpose (in plain words):**
- This class contains business logic for domain `Maintenance`. It probably interacts with one or more Repository interfaces and performs validations, transforms (DTO -> Entity), and transactions.

---

### `NotificationService.java` — *interface*
- **Path:** `TrackWise-main/TrackWise-main/backend/src/main/java/org/godigit/trackwise/service/NotificationService.java`
- **Package:** `org.godigit.trackwise.service`
- **Detected role(s):** Service / Business Logic

**Fields (approx.):** None detected or declared dynamically.

**Methods (approx.):** None detected.

**Purpose (in plain words):**
- This class contains business logic for domain `Notification`. It probably interacts with one or more Repository interfaces and performs validations, transforms (DTO -> Entity), and transactions.

---

### `ReportService.java` — *interface*
- **Path:** `TrackWise-main/TrackWise-main/backend/src/main/java/org/godigit/trackwise/service/ReportService.java`
- **Package:** `org.godigit.trackwise.service`
- **Detected role(s):** Service / Business Logic

**Fields (approx.):** None detected or declared dynamically.

**Methods (approx.):** None detected.

**Purpose (in plain words):**
- This class contains business logic for domain `Report`. It probably interacts with one or more Repository interfaces and performs validations, transforms (DTO -> Entity), and transactions.

---

### `WarrantyService.java` — *interface*
- **Path:** `TrackWise-main/TrackWise-main/backend/src/main/java/org/godigit/trackwise/service/WarrantyService.java`
- **Package:** `org.godigit.trackwise.service`
- **Detected role(s):** Service / Business Logic

**Fields (approx.):** None detected or declared dynamically.

**Methods (approx.):** None detected.

**Purpose (in plain words):**
- This class contains business logic for domain `Warranty`. It probably interacts with one or more Repository interfaces and performs validations, transforms (DTO -> Entity), and transactions.

---

### `AssetServiceImpl.java` — *class*
- **Path:** `TrackWise-main/TrackWise-main/backend/src/main/java/org/godigit/trackwise/service/impl/AssetServiceImpl.java`
- **Package:** `org.godigit.trackwise.service.impl`
- **Class annotations:** `Service, RequiredArgsConstructor, Transactional, Override, Override, Override, Override, Override, Override`
- **Detected role(s):** Service / Business Logic
- **Implements:** `AssetService`

**Fields (approx.):** None detected or declared dynamically.

**Methods (approx.):**
- `create(...)` — `public AssetResponse create(AssetRequest request) {` Annotations: `Override`
- `getById(...)` — `public AssetResponse getById(UUID id) {` Annotations: `Override`
- `list(...)` — `public Page<AssetResponse> list(Pageable pageable) {` Annotations: `Override`
- `update(...)` — `public AssetResponse update(UUID id, AssetRequest request) {` Annotations: `Override`
- `delete(...)` — `public void delete(UUID id) {` Annotations: `Override`
- `assignToEmployee(...)` — `public AssetResponse assignToEmployee(UUID assetId, UUID employeeId) {` Annotations: `Override`
- `unassign(...)` — `public AssetResponse unassign(UUID assetId) {` Annotations: `Override`
- `findByStatus(...)` — `public List<AssetResponse> findByStatus(AssetStatus status) {` Annotations: `Override`
- `findWithWarrantyExpiringBetween(...)` — `public List<AssetResponse> findWithWarrantyExpiringBetween(LocalDate from, LocalDate to) {` Annotations: `Override`

**Purpose (in plain words):**
- This class contains business logic for domain `AssetImpl`. It probably interacts with one or more Repository interfaces and performs validations, transforms (DTO -> Entity), and transactions.

---

### `CheckInOutServiceImpl.java` — *class*
- **Path:** `TrackWise-main/TrackWise-main/backend/src/main/java/org/godigit/trackwise/service/impl/CheckInOutServiceImpl.java`
- **Package:** `org.godigit.trackwise.service.impl`
- **Class annotations:** `Service, RequiredArgsConstructor, Transactional, Override, Override, Override, Transactional(readOnly = true), Override, Transactional(readOnly = true), Override`
- **Detected role(s):** Service / Business Logic
- **Implements:** `CheckInOutService`

**Fields (approx.):** None detected or declared dynamically.

**Methods (approx.):**
- `checkoutAsset(...)` — `public CheckInOutResponseDTO checkoutAsset(CheckInOutRequestDTO request) {` Annotations: `Override`
- `checkinAsset(...)` — `public CheckInOutResponseDTO checkinAsset(CheckInOutRequestDTO request) {` Annotations: `Override`
- `historyByAsset(...)` — `public List<CheckInOutResponseDTO> historyByAsset(UUID assetId) {` Annotations: `Override, Transactional(readOnly = true)`
- `historyByEmployee(...)` — `public List<CheckInOutResponseDTO> historyByEmployee(UUID employeeId) {` Annotations: `Override, Transactional(readOnly = true)`
- `processAssetScan(...)` — `public CheckInOutResponseDTO processAssetScan(AssetScanRequestDTO request) {` Annotations: `Override`

**Purpose (in plain words):**
- This class contains business logic for domain `CheckInOutImpl`. It probably interacts with one or more Repository interfaces and performs validations, transforms (DTO -> Entity), and transactions.

---

### `EmployeeServiceImpl.java` — *class*
- **Path:** `TrackWise-main/TrackWise-main/backend/src/main/java/org/godigit/trackwise/service/impl/EmployeeServiceImpl.java`
- **Package:** `org.godigit.trackwise.service.impl`
- **Class annotations:** `Service, RequiredArgsConstructor, Transactional, Override, Override, Transactional(readOnly = true), Override, Transactional(readOnly = true), Override, Override, Override, Transactional(readOnly = true)`
- **Detected role(s):** Service / Business Logic
- **Implements:** `EmployeeService`

**Fields (approx.):** None detected or declared dynamically.

**Methods (approx.):**
- `create(...)` — `public Employee create(EmployeeRequestDTO dto) {` Annotations: `Override`
- `getById(...)` — `public Employee getById(UUID id) {` Annotations: `Override, Transactional(readOnly = true)`
- `list(...)` — `public Page<Employee> list(Pageable pageable) {` Annotations: `Override, Transactional(readOnly = true)`
- `update(...)` — `public Employee update(UUID id, EmployeeRequestDTO dto) {` Annotations: `Override`
- `delete(...)` — `public void delete(UUID id) {` Annotations: `Override`
- `findByEmail(...)` — `public Optional<Employee> findByEmail(String email) {` Annotations: `Override, Transactional(readOnly = true)`

**Purpose (in plain words):**
- This class contains business logic for domain `EmployeeImpl`. It probably interacts with one or more Repository interfaces and performs validations, transforms (DTO -> Entity), and transactions.

---

### `IoTServiceImpl.java` — *class*
- **Path:** `TrackWise-main/TrackWise-main/backend/src/main/java/org/godigit/trackwise/service/impl/IoTServiceImpl.java`
- **Package:** `org.godigit.trackwise.service.impl`
- **Class annotations:** `Service, RequiredArgsConstructor, Transactional, Override, Override, Override, Override`
- **Detected role(s):** Service / Business Logic
- **Implements:** `IoTService`

**Fields (approx.):**
- `simulatorFuture` : `ScheduledFuture<?>` (private)

**Methods (approx.):**
- `ingest(...)` — `public IoTDataResponseDTO ingest(IoTDataRequestDTO request) {` Annotations: `Override`
- `processSensorData(...)` — `public IoTDataResponseDTO processSensorData(UUID assetId, Double temperature, Double batteryLevel, Boolean inUse, Double latitude, Double longitude) {` Annotations: `Override`
- `startSimulator(...)` — `public void startSimulator() {` Annotations: `Override`
- `stopSimulator(...)` — `public void stopSimulator() {` Annotations: `Override`
- `runSimulationStep(...)` — `private void runSimulationStep() {` 

**Purpose (in plain words):**
- This class contains business logic for domain `IoTImpl`. It probably interacts with one or more Repository interfaces and performs validations, transforms (DTO -> Entity), and transactions.

---

### `MaintenanceServiceImpl.java` — *class*
- **Path:** `TrackWise-main/TrackWise-main/backend/src/main/java/org/godigit/trackwise/service/impl/MaintenanceServiceImpl.java`
- **Package:** `org.godigit.trackwise.service.impl`
- **Class annotations:** `Service, RequiredArgsConstructor, Transactional, Override, Override, Transactional(readOnly = true)`
- **Detected role(s):** Service / Business Logic
- **Implements:** `MaintenanceService`

**Fields (approx.):** None detected or declared dynamically.

**Methods (approx.):**
- `addMaintenance(...)` — `public MaintenanceResponseDTO addMaintenance(UUID assetId, MaintenanceRequestDTO request) {` Annotations: `Override`
- `listByAsset(...)` — `public List<MaintenanceResponseDTO> listByAsset(UUID assetId) {` Annotations: `Override, Transactional(readOnly = true)`

**Purpose (in plain words):**
- This class contains business logic for domain `MaintenanceImpl`. It probably interacts with one or more Repository interfaces and performs validations, transforms (DTO -> Entity), and transactions.

---

### `NotificationServiceImpl.java` — *class*
- **Path:** `TrackWise-main/TrackWise-main/backend/src/main/java/org/godigit/trackwise/service/impl/NotificationServiceImpl.java`
- **Package:** `org.godigit.trackwise.service.impl`
- **Class annotations:** `Service, RequiredArgsConstructor, Transactional, Override, Override`
- **Detected role(s):** Service / Business Logic
- **Implements:** `NotificationService`

**Fields (approx.):** None detected or declared dynamically.

**Methods (approx.):**
- `createInAppNotification(...)` — `public NotificationResponseDTO createInAppNotification(NotificationRequestDTO request) {` Annotations: `Override`
- `sendEmail(...)` — `public void sendEmail(EmailRequestDTO request) {` Annotations: `Override`

**Purpose (in plain words):**
- This class contains business logic for domain `NotificationImpl`. It probably interacts with one or more Repository interfaces and performs validations, transforms (DTO -> Entity), and transactions.

---

### `ReportServiceImpl.java` — *class*
- **Path:** `TrackWise-main/TrackWise-main/backend/src/main/java/org/godigit/trackwise/service/impl/ReportServiceImpl.java`
- **Package:** `org.godigit.trackwise.service.impl`
- **Class annotations:** `Service, RequiredArgsConstructor, Transactional(readOnly = true), Override, Override`
- **Detected role(s):** Service / Business Logic
- **Implements:** `ReportService`

**Fields (approx.):** None detected or declared dynamically.

**Methods (approx.):**
- `generateWarrantyExpiryReport(...)` — `public byte[] generateWarrantyExpiryReport(LocalDate from, LocalDate to) {` Annotations: `Override`
- `generateAssetAgingReport(...)` — `public byte[] generateAssetAgingReport(int olderThanDays) {` Annotations: `Override`

**Purpose (in plain words):**
- This class contains business logic for domain `ReportImpl`. It probably interacts with one or more Repository interfaces and performs validations, transforms (DTO -> Entity), and transactions.

---

### `WarrantyServiceImpl.java` — *class*
- **Path:** `TrackWise-main/TrackWise-main/backend/src/main/java/org/godigit/trackwise/service/impl/WarrantyServiceImpl.java`
- **Package:** `org.godigit.trackwise.service.impl`
- **Class annotations:** `Service, RequiredArgsConstructor, Transactional, Override, Override, Transactional(readOnly = true), Override`
- **Detected role(s):** Service / Business Logic
- **Implements:** `WarrantyService`

**Fields (approx.):** None detected or declared dynamically.

**Methods (approx.):**
- `createOrUpdate(...)` — `public WarrantyResponseDTO createOrUpdate(WarrantyRequestDTO request) {` Annotations: `Override`
- `findExpiringBetween(...)` — `public List<WarrantyResponseDTO> findExpiringBetween(LocalDate from, LocalDate to) {` Annotations: `Override, Transactional(readOnly = true)`
- `extendWarranty(...)` — `public WarrantyResponseDTO extendWarranty(UUID warrantyId, LocalDate newEndDate) {` Annotations: `Override`

**Purpose (in plain words):**
- This class contains business logic for domain `WarrantyImpl`. It probably interacts with one or more Repository interfaces and performs validations, transforms (DTO -> Entity), and transactions.

---



**Total Java files processed:** 77
