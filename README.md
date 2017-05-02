@Transactional
	@Rollback(false)
	@Test
	public void getDocByID_UUIDParam_OutcomeObject(){		
		UUID id = this.insertProject();		
		assertNotNull(id);
		Project proj = this.getProject(id);
		checkEqual(proj);		
	}
